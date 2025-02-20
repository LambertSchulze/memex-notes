---
category: note
tags:
  - React
  - TypeScript
created: 2024-09-20
---
To pass on `children` in a React Component you can use Reacts `PropsWithChildren` Type.

```TS
const ProductTile = ({ children }: React.PropsWithChildren) => (
    <div>
	    {children}
    </div>
)
```

It can be used on its own or with other Properties

```TS
type Props = {
	title: string
}

const ProductTile = ({ title, children }: PropsWithChildren<Props>) => (
	<div>
	    <div>{title}</div>
	    {children}
    </div>
)
```


You can also type it explicitly in the Property Type using Reacts `ReactNode` Type

```TS
type Props = {
	title: string,
	children: React.ReactNode
}

const ProductTile = ({ title, children }: Props) => (
	<div>
	    <div>{title}</div>
	    {children}
    </div>
)
```

`ReactNode` is a Type that accepts any valid [[JSX]].