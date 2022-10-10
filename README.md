# jqDnR-touch-callback
### Minimalistic Drag'n'Resize for jQuery with callback functionality
===================================================

Forked from [gaarf](http://github.com/gaarf/jqDnR-touch) which was based on [jqDnR](http://dev.iceburg.net/jquery/jqDnR/) &copy; 2007 Brice Burgess &lt;bhb@iceburg.net&gt;

Licensed under the [MIT License](http://www.opensource.org/licenses/mit-license.php).

#### This version was slightly modified by @dylan-hepworth to provide a callback once the drag event has completed and the mouse has been released.

#### Usage:

if box is a DOM node that should be draggable:

```js
$(box).jqDrag();
```

if box is a DOM node that should be both draggable and resizable:

```js
$(box).jqDrag(moveHandle).jqResize(resizeHandle);
```

where moveHandle/resizeHandle are optional DOM elements. if not defined, the whole box will be used as handle.
  
#### jQuery synthesized events triggered:

 * `jqDnRstart`  drag/resize operation starts
 * `jqDnRend`  drag/resize operation ends
 * `jqDnRtop`  element brought to top (via click or touch) without drag

## Providing a Callback Function
```js
var myCallback = function() {
    alert("Done dragging!");
}

$(box).jqDrag(null, myCallback);
```