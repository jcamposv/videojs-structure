# videojs-structure

This will update the default video structure, this is perfect when you need to work with react and need to add new component into the video plugin tag, you will have
a clean structure to add custom component in individual wrapper and easy to apply custom styles.

## Table of Contents

<!-- START doctoc -->
<!-- END doctoc -->
## Installation

```sh
npm install --save videojs-structure
```

The npm installation is preferred, but Bower works, too.

```sh
bower install  --save videojs-structure
```

## Usage

To include videojs-structure on your website or web application, use any of the following methods.


### `<script>` Tag

This is the simplest case. Get the script in whatever way you prefer and include the plugin _after_ you include [video.js][videojs], so that the `videojs` global is available.

```html
<script src="//path/to/video.min.js"></script>
<script src="//path/to/videojs-structure.min.js"></script>
<script>
  var player = videojs('my-video');

  player.structure({customClass: 'vjs-custom-wrapper',moveControl: true});
</script>
```
## Options

You can pass the customClass name for the new wrap video and moveControl true to move the controls video to new parent.

### Browserify

When using with Browserify, install videojs-structure via npm and `require` the plugin as you would any other module.

```js
var videojs = require('video.js');

// The actual plugin function is exported by this module, but it is also
// attached to the `Player.prototype`; so, there is no need to assign it
// to a variable.
require('videojs-structure');

var player = videojs('my-video');

player.structure();
```

### RequireJS/AMD

When using with RequireJS (or another AMD library), get the script in whatever way you prefer and `require` the plugin as you normally would:

```js
require(['video.js', 'videojs-structure'], function(videojs) {
  var player = videojs('my-video');

  player.structure();
});
```

## License

MIT. Copyright (c) Jairo Campos Vargas


[videojs]: http://videojs.com/