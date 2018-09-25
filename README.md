rightclick-dragscroll
==========

Original implementation by: [Dmitry Prokashev](https://github.com/awersching/rightclick-dragscroll)

Dragscroll is a micro JavaScript library which
enables scrolling via holding the right mouse button ("drag and drop" or
"click and hold" style). It has no dependencies and
is written in vanilla JavaScript (which means it works anywhere).


### Usage

Make sure to disable the context menu (which is mapped to right click per default).


Download the and unpack or install it using npm:

or npm:

```sh
$ npm install rightclick-dragscroll
```

Load the `dragscroll.js` in a preferable way (that is an UMD module):

```html
<script src="path/to/dragscroll.js"></script>
```

Add the `dragscroll` class to a scrollable element:

```html
<div class=dragscroll>
    Big text goes here...
</div>
```

That's it! Now you can scroll it by dragging. You can also add the
`dragscroll` class to the `<body>` element and drag the whole page.

Keep in mind that now it is not possible to select the content with
mouse, so apply the `cursor: default;` CSS style to prevent confusing
the users (or even `cursor: grab;` in case the content is not a text).

If you add or remove the `dragscroll` class dynamically, invoke
`dragscroll.reset()` to update the listeners.

You can also add the `nochilddrag` attribute to a scrollable element,
which will only enable drag-scrolling for an element itself, but not
for its subchildren. This can be usefull, if you want to enable the
scrolling the area by dragging its empty space, but keep the
opportunity to select the text.
