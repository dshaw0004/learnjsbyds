---
slug: dataattribute
title: JavaScript Data Attribute
---

### Check a data attribute existance ?

To check if a element have a specific data attribute we can use `hasAttribute` method

```js
const nav = document.querySelector(".navbar");
if (nav.hasAttribute("data-visible")) {
	closeNavBar();
	nav.removeAttribute("data-visible");
} else {
	openNavBar();
	nav.dataset.visible = true;
}
```
