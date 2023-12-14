---
slug: commonerrorsandfixes
title: Common JS errors anf their fixes
---

#### React Error `Type 'MutableRefObject<HTMLUListElement | undefined>' is not assignable to type 'LegacyRef<HTMLUListElement> | undefined'``.

```js
const navUlRef = useRef < HTMLUListElement > null;
```
