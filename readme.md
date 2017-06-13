# How to use

This is an example site meant to explore how we include headings in Willow components and how we show or hide them.

1. `git pull` the latest from the [Unum Theme](https://github.com/unumux/theme-unum-default)
1. From the theme's directory in terminal run `npm link @unumux/theme-unum-default`
1. `git pull` the latest from the [Willow Repo](https://github.com/unumux/willow)
1. `git checkout default-visibility` to see the scratch work branch in Willow
1. `npm link @unumux/willow` after you are on the correct branch
1. `git clone` this repo (default-visibility)
1. From this repo's directory in terminal run the following:
   1. `npm link @unumux/theme-unum-default`
   1. `cd node_modules/@unumux/theme-unum-default`
   1. `npm link @unumux/willow`
1. `cd ../../../` and run `ux` from the default-visibility project