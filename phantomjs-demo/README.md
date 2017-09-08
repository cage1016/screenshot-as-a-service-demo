# phantomjs simple demo

[![asciicast](https://asciinema.org/a/136840.png)](https://asciinema.org/a/136840)

```js
var page = require('webpage').create()

page.viewportSize = {
    width: 640,
    height: 480
}

page.clipRect = {
    top: 0,
    left: 0,
    width: 640,
    height: 480
}

page.open('https://www.google.com', function () {
    page.render('google.com.png')
    phantom.exit()
});
```