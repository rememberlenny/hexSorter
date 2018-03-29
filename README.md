# hexSorter v1.0.0

### Original:
![alt text](https://raw.githubusercontent.com/dagthomas/hexSorter/master/images/unsorted_hexSorter.png "Unsorted Color Array")

### Sorted:
![alt text](https://raw.githubusercontent.com/dagthomas/hexSorter/master/images/sorted_hexSorter.png "Sorted Color Array")

## Installation
In a browser:
```html
<script src="hexSorter.js"></script>
```

Using npm:
```shell
$ npm i --save hexsorter
```

In Node.js:
```js
// Load the module.
const hexSorter = require('./hexSorter');
```

## Why hexSorter?

hexSorter was based on an old Adobe Kuler plugin in php. Rewritten to work with<br>
new technology.<br><br>

Its usage is to automagically sort colors by luminosity, to generate style<br>
sheets or vector fill/strokes.<br><br>

 * Sort colors by luminosity
 * Get brightest color from array
 * Get most saturated color from array
 * Get dullest bright color from array
 * Mix hexadecimal color values to create/diffuse colors
 <br>

## Usage
```js
const hexSorter = require('./hexSorter');
const log = console.log;
var colorArray = ["#516373", "#f2b999", "#f2e8c9", "#6c838c", "#f2f2f2"];

log("bright", hexSorter.mostBrightColor(colorArray));
log("saturated", hexSorter.mostSaturatedColor(colorArray));
log("bright dull", hexSorter.brightestDullColor(colorArray));
log("mix", hexSorter.colorMixer('#000000', '#FF0000', 65));

```
### Examples

sortcolors.js - NodeJS example, showing how sorting works
```shell
node sortcolors
```

![alt text](https://raw.githubusercontent.com/dagthomas/hexSorter/master/images/output_hexSorter.png "Sorted Color Array")

convtocss.js - NodeJS example, reading from file, outputting to css.
```shell
node convtocss
```

Outputs dagthomas.css based on color arrays in colors.txt (from an earlier Kuler project, nvrfrgt).

### ADobe Kuler Top 100 palettes, 2017 (nvrfrgt)
[Color Input](https://github.com/dagthomas/hexSorter/blob/master/input/colors.txt)

[CSS Output](https://github.com/dagthomas/hexSorter/blob/master/output/dagthomas.css)

![alt text](https://raw.githubusercontent.com/dagthomas/hexSorter/master/images/example_hexSorter.png "Example of palette applied to SVG")
