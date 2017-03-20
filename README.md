
# compute-size

 [![Support me on Patreon][badge_patreon]][patreon] [![Buy me a book][badge_amazon]][amazon] [![PayPal][badge_paypal_donate]][paypal-donations] [![Version](https://img.shields.io/npm/v/compute-size.svg)](https://www.npmjs.com/package/compute-size) [![Downloads](https://img.shields.io/npm/dt/compute-size.svg)](https://www.npmjs.com/package/compute-size)

> Helper tool for resizing the things.

## :cloud: Installation

```sh
$ npm i --save compute-size
```


## :clipboard: Example



```js
const computeSize = require("compute-size");

console.log(computeSize({
    // Wanted size
    width: 10
    // 40% of the screen height
  , height: "40%"
}, {
    // Object width (e.g. an image)
    width: 10
    // ..and the height
  , height: 50
}, {
    screen_size: {
        width: 100
      , height: 200
    },
    preserve_aspect_ratio: false
}));
// { width: 10, height: 80 }

console.log(computeSize({
    // Wanted size
    width: 10
    // 40% of the screen height
  , height: "40%"
}, {
    // Object width (e.g. an image)
    width: 10
    // ..and the height
  , height: 50
}, {
    screen_size: {
        width: 100
      , height: 200
    }
}));
// { width: 10, height: 50 }

console.log(computeSize({
    // Wanted size
   height: "100%"
}, {
    width: 10
  , height: 50
}, {
    screen_size: {
        width: 100
      , height: 400
    }
}));
// { width: 80, height: 400 }
```

## :memo: Documentation


### `computeSize(wantedSize, realSize, options)`
Computes a wanted size based on the object, pixel and screen sizes.

#### Params
- **Object** `wantedSize`: An object containing the following fields:
 - `width` (Number): The wanted width.
 - `height` (Number): The wanted height.
- **Object** `realSize`: An object containing the following fields:
 - `width` (Number): The existing object width (e.g. an image).
 - `height` (Number): The existing object height (e.g. an image).
- **Object** `options`: An object containing the following fields:
 - `screen_size` (Object): The screen size (defaults to terminal width and height):
  - `width` (Number): The screen width.
  - `height` (Number): The screen height.
 - `px_size` (Object): The pixel size.
  - `width` (default: `1`)
  - `height` (default: `1`)
 - `preserve_aspect_ratio` (Boolean): If `false`, the aspect ratio will not be preserved (default: `true`).
 - `fit_screen` (Boolean): If `false`, the result size will not fit to screen (default: `true`).

#### Return
- **Object** The result size:
 - `width` (Number): The computed width.
 - `height` (Number): The computed height.



## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :sparkling_heart: Support my projects

I open-source almost everything I can, and I try to reply everyone needing help using these projects. Obviously,
this takes time. You can integrate and use these projects in your applications *for free*! You can even change the source code and redistribute (even resell it).

However, if you get some profit from this or just want to encourage me to continue creating stuff, there are few ways you can do it:

 - Starring and sharing the projects you like :rocket:
 - [![PayPal][badge_paypal]][paypal-donations]—You can make one-time donations via PayPal. I'll probably buy a ~~coffee~~ tea. :tea:
 - [![Support me on Patreon][badge_patreon]][patreon]—Set up a recurring monthly donation and you will get interesting news about what I'm doing (things that I don't share with everyone).
 - **Bitcoin**—You can send me bitcoins at this address (or scanning the code below): `1P9BRsmazNQcuyTxEqveUsnf5CERdq35V6`

    ![](https://i.imgur.com/z6OQI95.png)

Thanks! :heart:


## :dizzy: Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:


 - [`image-to-ascii`](https://github.com/IonicaBizau/image-to-ascii)—A Node.JS module that converts images to ASCII art.

## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[badge_patreon]: http://ionicabizau.github.io/badges/patreon.svg
[badge_amazon]: http://ionicabizau.github.io/badges/amazon.svg
[badge_paypal]: http://ionicabizau.github.io/badges/paypal.svg
[badge_paypal_donate]: http://ionicabizau.github.io/badges/paypal_donate.svg
[patreon]: https://www.patreon.com/ionicabizau
[amazon]: http://amzn.eu/hRo9sIZ
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(https%3A%2F%2Fionicabizau.net)&year=2016#license-mit
[website]: https://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
