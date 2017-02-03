---
title: Using Semantic UI in Laravel(elixir + gulp)
date: 2017-02-03 22:32:10
tags: 
  - laravel
  - elixir
  - gulp
  - semantic-ui
---

- Create the Laravel project 
- Install the Semantic UI with npm

```bash
npm install semantic-ui —save
```

- Change the directory

```bash
cd resources/assets/themes/semantic/
```

- Build

```bash
gulp build
```

- When we execture the build command, we need to choose the build mode. I choose auto, and 
	- setup the project root to  default,
	- setup the resource to “resources/assets/themes/semantic” (We can see the semantic is build to resources folder)
- Setup the gulpfile.js


```javascript
elixir((mix) => {
    mix.sass('app.scss')
       .webpack('app.js');

    // Copy semantic ui resource to public
     mix.copy('resources/assets/themes/semantic/dist/semantic.js', 'public/js/semantic.js')
        .copy('resources/assets/themes/semantic/dist/semantic.css', 'public/css/semantic.css');
    mix.version(['public/js/semantic.js', 'public/css/semantic.css']);
});

var gulp = require('gulp');
// copy the semantic ui resoutce font to laravel css folder
gulp.task('fonts', function() {
    gulp.src(['resources/assets/themes/semantic/dist/themes/default/assets/fonts/**/*'])
    .pipe(gulp.dest('public/css/themes/default/assets/fonts'));
});
// copy the semantic ui resoutce images to laravel css folder
gulp.task('images', function() {
    gulp.src(['resources/assets/themes/semantic/dist/themes/default/assets/images/**/*'])
    .pipe(gulp.dest('public/css/themes/default/assets/images'));
});
```

