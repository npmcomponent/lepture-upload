*This repository is a mirror of the [component](http://component.io) module [lepture/upload](http://github.com/lepture/upload). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/lepture-upload`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# upload

  file upload and progress api

## Installation

    $ component install component/upload

## Events

  - `error` an error occurred
  - `abort` upload was aborted
  - `progress` (e) upload in progress (`e.percent`, `e.totalSize` etc)
  - `end` upload is complete

## API

### Upload(file)

  Initialize an `Upload` with the given `file`, where `file`
  is a `File` object, for example from a `input.files[0]` `FileList`.

```js
var upload = new Upload(file);
var upload = Upload(file);
```

### Upload#to(path, [fn])

  __POST__ the multipart upload to `path` and invoke `fn(err, res)`.

```js
upload.to('/upload');
upload.on('progress', reportProgress);
upload.on('end', done);
```

## Running tests

  Run the Express test server:

```
$ npm install
$ make test
```

# License

  MIT

