---
category: note
tags:
  - JS
created: 2024-09-30
---
The JS `in` operator returns true if the specified attribute is present in an Object.

If an Object `object` has a property with the name `key` you can test with

```JS
if (key in object) {
	// do stuff
}
```

The `in` operator does not look for Elements in Arrays!
