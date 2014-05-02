# Cirrus Theme for Bootstrap 3

Cirrus is a light, modern theme for Bootstrap 3 built on the [Themestrap](https://github.com/divshot/themestrap)
foundation. You can install it like so:

    bower install bootstrap-theme-cirrus

You can [see the GitHub pages](http://code.divshot.com/bootstrap-theme-cirrus/) for a live demo of how it looks and further instruction. Enjoy!

## Copyright and license

Copyright 2013 Divshot, Inc. under [the Apache 2.0 license](LICENSE).

## Updating Bootstrap
I removed the bootstrap dependency from `bower.json`, e.g.

```json
  "dependencies": { "bootstrap": "3.1.1" }
```

...because I do not want to pull it down as a transitive dependency.  Bootstrap is compiled into the distribution css here anyway -- why do I need to pull it in again (it also pulls in jQuery and I don't want that either).  Thus, if you want to update to a newer bootstrap, the easiest way is to add it back into `bower.json` -- one time only (if bower had something like `devDependency` that would be nice.  Then do `bower install`, manually run the `grunt copy` command, and make any hand-edits to the bootstrap less source you like (e.g. remove glyphicons).

Then, run `grunt` (default task) to rebuild the distribution css, remove the dependency from `bower.json` and commit.

## Updates

* v3.1.1 -- updated to Bootstrap 3.1.1, removed glyphicons (just import [font awesome from bootstrap cdn](https://fortawesome.github.io/Font-Awesome/get-started/)).  
  
