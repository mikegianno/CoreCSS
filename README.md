# CoreCSS
A css barebone framework to kickstart any new project. Very often you come up with an idea that you want to easily kickstart/test. This framework will get you to step 2 instead of starting at step 0 and building all over the same structure.

## Base

What this framework will be is a set of CSS rules and folder structure. The logic is based on OOCSS and uses Sass extension language.

## Idea

Will try to perform an easily maintainable and stable CSS core to base any new project on it. I will try to explain and reason each folder and each file.

## What CoreCSS will NOT BE

This framework cannot support your entire projects. It will simply set the basic rules from where you can continue development.


## Folders explanation

### config/core

Contains all the core variable values that will be used in ALL projects. This means that the proposed values affect the whole of any project/application. Consider any changes inside the core subfolder as an **alert to check your codebase**.

### config

Contains all variables that will be ACTUALLY used inside the application. Each file in config requires that a same file exists in the core subfolder. Usage example:

config/colors.scss should have a line on top importing the config/core/colors.scss

### base

Contains files like reset, init, grid(mere suggestion for a grid), [icons] placeholder file, blocks mixins file.

blocks.scss - is a proposal that contains mixins for repeatable 'types' of elements. Each mixin describes an abstract style shared among many elements.

### utilities

Contains single css rule styles only!

### objects

Set of abstract objects style and responsive behavior.

### components

Placeholder folder to fill up with specific implementations/solutions of a UI problem found in more
than one pages. Examples, modals, carousels, navigation lists

### views

Placeholder folder to fill up with UIs referring to very specific views and pages. That is, if you
have a specific page that needs some specific solution you should be adding it in here. A good rule you could set is to allow an element to be called a view if it's found less than X times in your markup, otherwise this element should be a component. I feel this X should be 2 or 3.
*So if an  element is repeated more than 3 times in markup it should NOT be a view but a component.*
