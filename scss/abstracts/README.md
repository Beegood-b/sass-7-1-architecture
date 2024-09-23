# The *abstracts* folder contains foundational SCSS files that define variables, functions, and mixins. These files provide a global framework for styling throughout the project, promoting consistency and reducing code duplication. The contents of this folder are typically not compiled into CSS directly but are imported into other SCSS files as needed.

## Files in *abstracts*:

### _breakpoints.scss:
Contains predefined media query breakpoints for responsive design. These breakpoints help manage how the layout and components respond to different screen sizes (mobile, tablet, desktop, etc.).

### _colors.scss:
Defines the color palette for the project. This file centralizes the project's color scheme, making it easy to update or reference colors consistently across the entire codebase.

### _functions.scss:
Contains reusable SCSS functions. These are small, reusable pieces of logic (like math or string manipulation) that can be used throughout the stylesheets to enhance code flexibility and reusability.

### _mixins.scss:
Holds SCSS mixins for reusable code snippets. Mixins help to avoid code repetition by allowing blocks of SCSS code to be reused in multiple places (e.g., for media queries, gradients, or vendor prefixes).

### _type.scss:
Manages typography-related variables and mixins such as font sizes, font families, line heights, and text utilities. This ensures consistent typography across the project.

### _vars.scss:
Defines general-purpose variables used throughout the project. This file can contain variables for spacing, z-indexes, transitions, or other reusable values, making updates easier and maintaining consistency.