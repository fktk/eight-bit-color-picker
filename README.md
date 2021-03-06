Eight Bit Color Picker
======================

> UI component for picking a color from arbitrary 256 color palettes

![palette image](palette.png)

[このリポジトリ](https://github.com/bilalq/eight-bit-color-picker)をクローンして、自作アプリで使い勝手がよくなるように修正しました。
うまくminifyできなかったので、libから直接使うといいかと思います。

This is a simple, flexible color-picker widget. It has no dependencies (not
even on jQuery), so it's easy to just plug in and use. It weighs less than 3kb
of combined JS & CSS once minified and gzipped.

Since it exposes itself via the
[UMD](https://github.com/umdjs/umd/blob/master/returnExports.js) exports format,
it will comply with whatever module loading system you're using. If you're
not using one, it will expose a global called `EightBitColorPicker`.

Install
-------

```sh
npm install fktk/eight-bit-color-picker
```

Quick Start
-----------
You can pass in either a string of an element ID or a reference to a DOM
element into the constructor of `EightBitColorPicker` like so:

```html
<div id="target"></div>
```

```javascript
// You can do this
var ebcp = new EightBitColorPicker({ el: 'target' })

// Or this
var el = document.getElementById('target')
var ebcp = new EightBitColorPicker({ el: el })
```

Alternatively, you can just run the `detect` function to find all elements with
the class `eight-bit-color-picker` and instantiate them as pickers.

```html
<div class="eight-bit-color-picker"></div>
<div class="eight-bit-color-picker"></div>
```

```javascript
// Renders all color pickers
var pickers = EightBitColorPicker.detect()
```

Custom Palettes
---------------
The documentation goes into this in more detail, but you can easily customize
the color palette on a per picker basis. For those interested in writing web
apps that relate to the CLI, see
[this xterm-256color palette](https://github.com/bilalq/xterm-256color-palette).

```javascript
var customPalette = [ /* Some array of 256 hex color strings */ ]
var picker = new EightBitColorPicker({ el: 'target', palette: customPalette })
```

You can even update the palette of an already instantiated picker by invoking
`EightBitColorPicker.prototype.updatePalette`.

Documentation
-------------
フォーク元様のマニュアルです。

See [this page](http://bilalq.github.io/eight-bit-color-picker/) for documentation.

License
-------
[MIT](LICENSE)
