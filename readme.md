# Heading (Or Any Element) Visibility Example

This is an example site meant to explore how we include headings in Willow components and how we show or hide them.

## Setup

1. `git pull` the latest from the [Unum Theme](https://github.com/unumux/theme-unum-default)
1. From the theme's directory in terminal run `npm link`
1. `git pull` the latest from the [Willow Repo](https://github.com/unumux/willow)
1. `git checkout default-visibility` - this is the branch in Willow where this scratch work was done.
    - _It is important that you do not switch to another branch on Willow while running UX in this project (step 8) or else it will not pull the correct styling._
1. `npm link` after you are on the correct branch
1. In a new terminal window, `git clone` this repo [heading-visibility](https://github.com/unumux/heading-visibility)
1. From this repo's directory in terminal run the following:
   1. `npm link @unumux/theme-unum-default`
   1. `cd node_modules/@unumux/theme-unum-default`
   1. `npm link @unumux/willow`
1. `cd ../../../` and run `ux` in the heading-visibility project

## Examples to Review

Check out the HTML in this repo's code to see the components in action, and then check out the code on the default-visibility branch in Willow to see how it works behind the scenes.

- Primary Navigation
- Breadcrumbs
- Secondary Navigation
- Footer Navigation

## Accessibility Research Results

Component blocks that are made from sectioning elements require a heading for semantics – these headings are announced as a title of the component.

Component blocks that do not have/require a heading can use `aria-label` to provide more information to the user if necessary.

`aria-label` can also work as a clarifying attribute to be used along side the `role` attribute. So f we have `role="navigation"` on multiple components on a single page, we can use `aria-label` to give more clarity of purpose.  A screen reader would announce “Site Navigation Landmark” when `role=“navigation”` and `aria-label=“site”` are used.

We could use `aria-labelledby` to forgo using `aria-label` – but this would require the addition of the `id` attribute to the component’s heading element.  We do not use `id` attributes on Willow components to avoid repeated id’s on a page.  So we should not use `aria-labelledby` in Willow - but we can give clear instruction on how to use it via the accessibility site to allow developers to use it for their own components/html.