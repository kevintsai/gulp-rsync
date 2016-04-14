## gulp-rsync with multi-targets support

This is a patch for [gulp-rsync](https://github.com/jerrysu/gulp-rsync) that supported multi-targets.

### Prerequisites

rsync needs to be installed on your machine.

### Installation

```
npm install --save-dev git+https://github.com/kevintsai/gulp-rsync
```

### Usage

Use `hostnames` instand of `hostname` for setting multi-targets.

```js
var gulp = require('gulp');
var rsync = require('gulp-rsync');

gulp.task('deploy', function() {
  gulp.src('build/**')
    .pipe(rsync({
      root: 'build',
      hostnames: ['example1.com', 'example2.com'],
      destination: '/path/to/site'
    }));
});
```

Please reference [gulp-rsync](https://github.com/jerrysu/gulp-rsync) for more information.