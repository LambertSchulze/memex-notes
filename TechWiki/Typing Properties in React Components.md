---
category: note
tags:
  - React
  - TypeScript
created: 2024-09-20
---
```TS
type Props = {
  title: string
  description?: string
}

function ProductTile({ title, description }: Props) {
  return (
    <div>
      <div>{title}</div>
      {description && <div>{description</div>}
    </div>
  )
}
```


Without a defined Prop Type

```TS
function ProductTile({ title, description }: {
  title: string
  description?: string
}) => {
  return (
    <div>
      <div>{title}</div>
      {description && <div>{description</div>}
    </div>
  )
}
```


If written as _Function Component_ you could use Reacts `FC` Type

```TS
type Props = {
  title: string
  description?: string
}

const ProductTile: React.FC<Props> = ({
	title,
	description
}) => (
    <div>
	    <div>{title}</div>
	    {description && <div>{description</div>}
	</div>
)
```


Sometimes the Properties are special.
Maybe they have to be [[Passing Children in React Components|rendered Child Components]].
Or you have to pass a whole [[Passing Components as Property in React Components|Component as a Property]].

[[Piping Properties to Child Components in React]]
