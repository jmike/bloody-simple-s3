# Bloody simple S3

A bloody simple S3 client, based on the official AWS SDK.

[ ![Build Status for visionmobile/bloody-simple-sqs](https://codeship.com/projects/ce3c9d80-bb71-0132-8afa-3ee0b98d9f7e/status?branch=master)](https://codeship.com/projects/72166)

#### Features

* Promise and callback interface;
* Automatic file integrity check;
* Bloody simple API.

## Quick start

```javascript
var S3 = require('bloody-simple-s3');

var s3 = new S3({
  bucket: 'bucket-name',
  region: 'us-east-1',
  accessKeyId: 'AKIA-access-key',
  secretAccessKey: 'secret-access-key',
  sslEnabled: true
});

s3.upload('/Users/john/Photos/monkey.jpg', 'images/monkey-1.jpg')
  .then(function (file) {
    console.log(file.name);
  })
  .catch(function (err) {
    console.error(err);
  });
```

For further information on how to use this library please refer to the [API docs](https://github.com/visionmobile/bloody-simple-s3/blob/master/docs/API.md).

## Installation

```
$ npm install bloody-simple-s3
```

#### Requirements

* Node.js 0.8+

## Contribute

Source code contributions are most welcome. The following rules apply:

1. JavaScript source code needs to follow the [Airbnb Style Guide](https://github.com/airbnb/javascript);
2. Functions need to be well documented in [API docs](https://github.com/visionmobile/bloody-simple-s3/blob/master/docs/API.md);
3. Unit tests are necessary.

## Support

If you are having issues with this library, please let us know.

* Issue Tracker: [github.com/visionmobile/bloody-simple-s3/issues](https://github.com/visionmobile/bloody-simple-s3/issues)

## License

MIT
