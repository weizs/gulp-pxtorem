# gulp-pxtorem-plus [![NPM version](https://badge.fury.io/js/gulp-pxtorem-plus.svg)](http://badge.fury.io/js/gulp-pxtorem-plus)

This is a Gulp plugin for [postcss-pxtorem-plus](https://github.com/weizs/postcss-pxtorem-plus).

### Installation

```shell
npm install gulp-pxtorem-plus --save-dev
```

### Example

```js
var pxtorem = require('gulp-pxtorem-plus');

gulp.task('css', function() {
    gulp.src('css/**/*.css')
        .pipe(pxtorem())
        .pipe(gulp.dest('css'));
});
```

### Options

Pass in two option objects. The first one for [postcss-pxtorem-plus](https://github.com/weizs/postcss-pxtorem-plus) options, the second for [postcss](https://github.com/postcss/postcss) options.

```js
var pxtorem = require('gulp-pxtorem-plus');

var pxtoremOptions = {
    replace: false
};

var postcssOptions = {
    map: true  
};

gulp.task('css', function() {
    gulp.src('css/**/*.css')
        .pipe(pxtorem(pxtoremOptions, postcssOptions))
        .pipe(gulp.dest('css'));
});
```
