# CSS

## HTML Document flow block and inline

### block:

- div
- form
- h1...h6

### inline:

- a
- img
- input
- label
- b
- i
- em
- span



## Block, Element, Modifier (BEM Methodology)

[https://en.bem.info/methodology/quick-start/#modifier](https://en.bem.info/methodology/quick-start/#modifier)

### Block

A functionally independent page component that can be reused. In HTML, blocks are represented by the `class` attribute.

Features:

* The [block name](https://en.bem.info/methodology/naming-convention/#block-name) describes its purpose ("What is it?" — `menu` or `button`), not its state ("What does it look like?" — `red` or `big`).
* The block shouldn't influence its environment, meaning you shouldn't set the external geometry (margin) or positioning for the block.
* You also shouldn't use CSS tag or `ID` selectors when using BEM.

### Element

A composite part of a block that can't be used separately from it.

Features:

* The [element name](https://en.bem.info/methodology/naming-convention/#element-name) describes its purpose ("What is this?" — `item`, `text`, etc.), not its state ("What type, or what does it look like?" — `red`, `big`, etc.).
* The structure of an element's full name is `block-name__element-name`. The element name is separated from the block name with a double underscore (`__`).

### Modifier

An entity that defines the appearance, state, or behavior of a block or element.

Features:

* The [modifier name](https://en.bem.info/methodology/naming-convention/#block-modifier-name) describes its appearance ("What size?" or "Which theme?" and so on — `size_s` or `theme_islands`), its state ("How is it different from the others?" — `disabled`, `focused`, etc.) and its behavior ("How does it behave?" or "How does it respond to the user?" — such as `directions_left-top`).
* The modifier name is separated from the block or element name by a single underscore (`_`).

## BEM tree

[https://en.bem.info/methodology/key-concepts/#bem-tree](https://en.bem.info/methodology/key-concepts/#bem-tree)

A representation of a web page structure in terms of blocks, elements, and modifiers. It is an abstraction over a [DOM tree](https://en.wikipedia.org/wiki/Document_Object_Model) that describes the names of BEM entities, their states, order, nesting, and auxiliary data.

In real-life projects, a BEM tree can be presented in any format that supports the tree structure.

Let's consider an example of a DOM tree:

```
<header class="header">
    <img class="logo">
    <form class="search-form">
        <input class="input">
        <button class="button"></button>
    </form>
    <ul class="lang-switcher">
        <li class="lang-switcher__item">
            <a class="lang-switcher__link" href="url">en</a>
        </li>
        <li class="lang-switcher__item">
            <a class="lang-switcher__link" href="url">ru</a>
        </li>
    </ul>
</header>
```

The corresponding BEM tree will look like this:

```
header
    logo
    search-form
        input
        button
    lang-switcher
        lang-switcher__item
            lang-switcher__link
        lang-switcher__item
            lang-switcher__link
```
