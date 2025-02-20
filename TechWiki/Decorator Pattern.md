---
category: note
tags:
  - DesignPatterns
  - SoftwareArchitecture
created: 2024-09-18
---
> The decorator pattern allows you to attach new behaviors to objects by placing these objects inside special _wrapper_ objects that contain the behaviors.

> The decorator pattern is like an intentional man-in-the-middle attack. You replace a class with your _custom_ implementation, run some code, then call the true method.

Das Decorator Pattern gehört zu den [[Design Patterns#Behavioral Patterns]].

Damit die Decoration funktionieren kann muss sowohl die original Klasse, als auch die dekorierte Klasse dasselbe Interface implementieren.

```php
class Bakery implements BakeryInterface
{
	public function bakeBread(string $type): Bread
	{
		// ...
	}
}

class DecoratedBakery implements BakeryInterface
{
	public function __construct(
		private Bakery $bakery;
	){}

	public function bakeBread(string $type): Bread
	{
		$bread = $this->bakery->bakeBread($type);

		// some work

		return $bread;
	}
}
```

