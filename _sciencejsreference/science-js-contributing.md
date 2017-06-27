---
title: Guidelines
subject: Reference
topics: Contributing
summary: Have a cool feature to add to the library? Before submitting a pull request, read through here first.
nice-name: science-js-lib-contributions
contributors:
updated: 2017-04-05
layout: post
---


# Contributing

If you think you have a nice feature to add to `science.js`, then here are some tips on how to add it:

1. The library is built from several smaller js files contained in the `src` folder. For example, the arrows are made by code found in the `arrow.js` file.

2. These files get consolidated into one big file: `science.js`

3. This is done using *grunt*. (Grunt will also tidy the src files and make a minified version of the science.js code.)

4. In short, _don't put your changes in the science.js file, but rather in a src file in the src folder.

5. Your additions should come with a few examples too, that show how it is used. These don't have to be (and shouldn't be) full fledged sims, but instead, super simple demos that highlight the important aspects of the science object.


# Conventions

To maintain uniformity, please use the following conventions.

1. File and folder naming. As suggested by google, please use dashes, not underscores to separate words in a file or directory name. i.e. `super-sim` not `super_sim` or `supersim`.

2. Variable naming. As per Javascript standard, please use camelcase rather than snakecase. For example, `myRadVariable,` not `my_rad_variable.`

3. Please use two spaces to indent when writing code for @examples in JSDoc. (Check for lurking tabs if the white space is coming out weird post JSDocing.) You'll also need to include a single space between the "*" and your "//" for it to compile comments ok. 