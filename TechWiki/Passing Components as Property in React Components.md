---
category: note
tags:
  - React
  - TypeScript
created: 2024-09-20
---
JSX can be typed with Reacts `ReactNode` Type

```TS
interface LayoutProps {
  nav: React.ReactNode;
  children: React.ReactNode;
}

const Layout = (props: LayoutProps) => {
  return (
    <>
      <nav>{props.nav}</nav>
      <main>{props.children}</main>
    </>
  );
};

<Layout nav={<h1>My Site</h1>}>
  <div>Hello!</div>
</Layout>;
```

You can also type the `children` like this, [[Passing Children in React Components|but you don't have to]].
There is also Reacts `PropsWithChildren` Type.

---
Passing a React Component would look like this:

```TS
interface UserIconProps {
	className?: string;
}

const UserIcon = ({ className }: UserIconProps) => (
	<div className={className} ></div>
);

  

interface RowProps {
	icon: React.ComponentType<UserIconProps>;
}

const Row = ({ icon }: RowProps) => {
	const Icon = icon;

	return (
		<div>
			<Icon className="h-8 w-8" />
		</div>
	);
};

<Row icon={UserIcon} />;
```

`React.ComponentType<UserIconProps>` means that `icon` is a React Component with the Interface `UserIconProps`.

You can't use `icon` directly because TS will say it doesn't exist on `JSX.IntrinsicElements`.

As alternative use the `props` Object

```TS
const Row = (props: RowProps) => {
	return (
		<div>
			<props.icon className="h-8 w-8" />
		</div>
	);
};
```

---
With Reacts `ElementType` Components _or_ native [[HTML tags]] can be passed

```TS
interface RowProps {
	element: React.ElementType<{
		className?: string;
	}>
}

const Row = (props: RowProps) => {
	return (
		<div>
			<props.element className="h-8 w-8" />
		</div>
	);
};

<Row element={'span'} />;
<Row element={UserIcon} />;
```

