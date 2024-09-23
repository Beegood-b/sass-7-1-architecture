# The *base* folder contains essential global styles that lay the foundation for the entire project. These styles are applied universally, ensuring consistency in default styling across all elements. This folder typically includes styles that apply to HTML elements, default browser resets, and base typography settings.

## Files in *base*:
### _fonts.scss:
Defines and imports the project's fonts, including web fonts and any custom fonts used. This file ensures consistent typography throughout the project by centralizing font declarations.

### _general.scss:
Contains general-purpose styles that apply to common elements like body, p, a, and basic layout structures. It can also include base utility classes and helper styles that don't fit into specific components or layouts.

### _reset.scss:
A CSS reset or normalization file that ensures consistent styling across different browsers by resetting or normalizing the default styles applied by browsers. This helps to create a predictable starting point for your custom styles.

### _root.scss:
Declares the root-level CSS variables (usually in the :root selector) for the project. These variables can be things like colors, font sizes, spacing units, and other values that will be used across the project.

### _typography.scss:
Focuses on base typography styles, setting rules for headings (h1 to h6), paragraphs, lists, and other text elements. This file ensures consistent font sizing, line heights, and text alignment across the project.