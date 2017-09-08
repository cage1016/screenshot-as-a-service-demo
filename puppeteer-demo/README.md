# puppeteer simple demo

[![asciicast](https://asciinema.org/a/136850.png)](https://asciinema.org/a/136850)

```js
const puppeteer = require('puppeteer');

(async () => {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.goto('https://www.google.com');
  await page.screenshot({path: 'google.com.png'});

  browser.close();
})();
```