# Image Copy and Optimization Task
Copy image resources to build directory and optimizes them.

## API

### imageCopyOptimize([options])

Returns a [stream](http://nodejs.org/api/stream.html) of [Vinyl files](https://github.com/wearefractal/vinyl-fs)
that can be [piped](http://nodejs.org/api/stream.html#stream_readable_pipe_destination_options).

#### Available options:
- **src** (String|Array) Glob or array of globs ([What's a glob?](https://github.com/isaacs/node-glob#glob-primer)) matching image source files. Default: `'resources/www/img/**/*'`.
- **dest** (String) Output path for the HTML files. Default: `'www/img'`.

## Example

```
var imageCopyOptimize = require('ionic-gulp-image-task');

gulp.task('image', imageCopyOptimize);

gulp.task('image', function(){
  return imageCopyOptimize({ dest: 'www/my-custom-build-dir'});
});
```
