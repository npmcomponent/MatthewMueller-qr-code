
# qr-code

  Generate QR codes. Based on Kazuhiko Arase's [implementation](http://d-project.googlecode.com/svn/trunk/misc/qrcode/js/).

## Installation

    $ component install matthewmueller/qr-code

## Example

```js
var qr = require('qr-code');
var dataURI = qr('Hello!');
var img = new Image();
img.src = dataURI;
document.body.appendChild(img);
```

## API

QR(text, options)

Create a QR code containing the given `text`. The result is a dataURI that you can place in an image or background. QR also takes some `options` including:

- type: QR code type. Changes the amount of information you can store in the QR code. Defaults to `4`.
- level: Backup level. See [QR code error correction](http://www.qrstuff.com/blog/2011/12/14/qr-code-error-correction). Defaults to `M`
- size: Size of the QR code. Defaults to `4`.
- margin: Whitespace around the outside of the image. Defaults to `0`.

## License

  MIT