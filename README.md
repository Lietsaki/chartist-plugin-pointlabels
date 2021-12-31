# Point Labels plugin for Chartist.js (Improved Fork)

**Point Labels Plugin: Fork to correctly position values on top of bar charts and allow values of 0 (zero) by [Lietsaki](https://github.com/Lietsaki).**

[Original Plugin by GionKunz](https://github.com/gionkunz/chartist-plugin-pointlabels) (has not been maintained since 2018 at the time of writing this, Dec 31st 2021) 

This is a simple plugin for Chartist.js that will put a label on top of data points on line charts. This plugin serves
as an example plugin package and can be used as starting point to create your own awesome Chartist.js plugin.

Please visit http://gionkunz.github.io/chartist-js/plugins.html for more information.

## Download 
The easiest way to get started, using npm
```
npm i chartist-plugin-pointlabels-topbars
```

## Available options and their defaults

```javascript
var defaultOptions = {
  labelClass: 'ct-label',
  labelOffset: {
    x: 0,
    y: -10
  },
  textAnchor: 'middle',
  labelInterpolationFnc: Chartist.noop
};
```

## Sample usage in Chartist.js

```javascript
var chart = new Chartist.Line('.ct-chart', {
  labels: [1, 2, 3, 4, 5, 6, 7],
  series: [
    [1, 5, 3, 4, 6, 2, 3],
    [2, 4, 2, 5, 4, 3, 6]
  ]
}, {
  plugins: [
    ctPointLabels({
      textAnchor: 'middle',
      labelInterpolationFnc: function(value) {return '$' + value.toFixed(2)}
    })
  ]
});
```
