The css design system is based on ITCSS and BEM and also on personal preferences.
It mix a global css system and some atomic design

ITCSS architecture, we import everythind in the main.scss, each child of parts
can be either a file or a directory :

-styles // All the default and global styles
  |_ parts  // All the partials
    |_ vars
    |_ tools
    |_ resets
    |_ elements
    |_ objects
    |_ layouts
    |_ components
    |_ utilities
  |_ main.scss


Vars
Define the default values for the system. This is the same as settings

Tools
Globally used functions and mixins

Resets
Normalize and reset the css

Elements
Contains the styles of generics elements like body or html. It should contain only
generic rules that apply for every elements.

Objects
Not sure if I need it, but probably. We could define very generic "components"
like a media (image on the left and text on the right). It is linked to
the repetitive patterns of our application

Layouts
Contains rules about the display of a page, it should correspond with our layout
components. Kind of superComponent styles. We will have a layout for each page.
It is probably interesting to base this layout on css-grid.

Components
We import here every components styles. But each file is located in the same
folder than the jsx/tsx component it is related to.
Component style should use the BEM/SUIT CSS style PascalCase to match component
name in jsx/tsx :
  ComponentName
  ComponentName-child
  ComponentName--modifier
  ComponentName.is-stateOfComponent

Utilities
Some utility classes and mixins that can override any classes declared before. Maybe useful
for .hide or .h1
