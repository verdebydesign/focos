# Focos

Add focus to elements on the screen referenced by coordinates

## Usage

```html
    ...
    <div data-focos-cell="0,1">D</div>
    <div data-focos-cell="1,1">E</div>
    <div data-focos-cell="2,1">F</div>
    <div data-focos-cell="0,0">A</div>
    <div data-focos-cell="1,0">B</div>
    <div data-focos-cell="2,0">C</div>
    ...
```

```js
// Initialize focos
...
window.Focos({
    keys: { // optional | default arrow keys
      w: 'up',
      a: 'left',
      d: 'rigth',
      z: 'down'
    },
    gridSize: '2x1', // required | if bad value fallbacks to '1x1'
    step: 1, // optional | default '1'
    focusOnClick: true, // optional | default 'false'
    initialFocus: [0, 1] // optional | default 'undefined'
}, (target, cell) => {
    /* optional callback */
});
...
```

Focos will read the HTML above and create a 2x1 grid navigable by the keys "w,a,d,z".
Cell "0,1" will get initial focus, meaning will be focused on render.

## Author

&copy; 2019 Simao Nziaka
