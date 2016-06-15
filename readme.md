# rev-path-v

modified by rev-path, for generating md5 filename like
```
***.css?v=fcc1a7c477
***.js?v=ae6237e734
```

## Install

```
$ npm install --save rev-path-v
```


## Usage

This package is work with `gulp-rev-v` & `gulp-rev-collector-v`

```js
var revPath = require('rev-path-v');
var hash = 'bb9d8fe615'

var path = revPath('src/unicorn.png', hash);
//=> 'src/unicorn-bb9d8fe615.png'

revPath('src/unicorn.png', Date.now());
//=> 'src/unicorn-1432309925925.png'

// you can also revert an already hashed path
revPath.revert(path, hash);
//=> 'src/unicorn.png'
```


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
