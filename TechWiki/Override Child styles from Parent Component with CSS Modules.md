---
category: note
tags: CSS, CSSModules
created: 2024-09-27
---
Definier in jeder Component die default styles mit einer eigenen Classname.
Verschachtel die Classnames nicht ineinander.
Das erhöht nur unnötig die Specifizität.

```
.card {
	// card styles
}

.title {
	// title styles
}

.body {
	// body styles
}
```

```
import styles from './card.modules.css'

export const Card = ({title, children}) => (
	<article className={styles.card}>
		<h3 className={styles.title}>{title}</h3>
		<div className={styles.body}>
			{children}
		</div>
	</article>
);
```

Um die Card von außen stylebar zu machen, muss man ihr eine classname mitgeben können.

```
export const Card = ({title, children, externalClassName}) => (
	<article className={`${styles.card} ${externalClassName}`}>
		<h3 className={styles.title}>{title}</h3>
		<div className={styles.body}>
			{children}
		</div>
	</article>
);
```

Benutzt man die Card Component nun in einer anderen Component, kann die Parent Component ihr einen CSS className mitgeben.
Die styles werden in den Parent CSS styles aber einmal verschachtelt.
Dadurch erhalten sie eine höhere Spezifität.

```
.wrapper {
	// wrapper styles
}

.wrapper .childCard {
	// styles that override card styles
}
```

```
import styles from './wrapper.modules.css'
import Card from './card.tsx'

export const Wrapper = () => (
	<section className={styles.wrapper}>
		<Card externalClassName={styles.childCard} />
	</section>
);
```
