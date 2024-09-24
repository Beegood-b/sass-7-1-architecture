<div align="center">

# SASS 7-1 Architecture 
<img src="https://img.icons8.com/?size=100&id=QBqFNfPPB2Kx&format=png&color=000000" alt="" width="150">

</div>

## Overview

This project is structured using SCSS (Sass) to organize and manage styles efficiently. The SCSS files are grouped into folders that serve specific purposes, ensuring clean, maintainable, and scalable styles. This README outlines the structure and purpose of each folder and its contents.

## Table of Contents

- [Overview](#overview)
- [Folder Structure](#folder-structure)
  - [abstracts](https://github.com/Beegood-b/sass-7-1-architecture/tree/main/scss/abstracts)
  - [base](https://github.com/Beegood-b/sass-7-1-architecture/tree/main/scss/base)
  - [components](https://github.com/Beegood-b/sass-7-1-architecture/tree/main/scss/components)
  - [layout](https://github.com/Beegood-b/sass-7-1-architecture/tree/main/scss/layout)
  - [pages](https://github.com/Beegood-b/sass-7-1-architecture/tree/main/scss/pages)
  - [utils](https://github.com/Beegood-b/sass-7-1-architecture/tree/main/scss/utils)
  - [vendors](https://github.com/Beegood-b/sass-7-1-architecture/tree/main/scss/vendors)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Folder Structure

```
scss/
├── abstracts/
│   ├── _index.scss           # Forwarding all abstracts styles
│   ├── _breakpoints.scss     # Media Query Breakpoints
│   ├── _colors.scss          # Color Palette
│   ├── _functions.scss       # Sass Functions
│   ├── _mixins.scss          # Sass Mixins
│   ├── _type.scss            # Type scale rules
│   └── _vars.scss            # General-purpose variables
├── base/
│   ├── _index.scss           # Forwarding all base styles
│   ├── _fonts.scss           # Font definitions
│   ├── _general.scss         # General base styles
│   ├── _reset.scss           # Reset/normalize
│   └── _typography.scss      # Base typography rules
├── components/
│   ├── _index.scss           # Forwarding all components styles
│   ├── _buttons.scss         # Button styles
│   ├── _cards.scss           # Card styles
│   ├── _forms.scss           # Form styles
│   ├── _inputs.scss          # Input styles
│   └── _modals.scss          # Modal styles
├── layout/
│   ├── _index.scss           # Forwarding all layout styles
│   ├── _breadcrumbs.scss     # Breadcrumb navigation
│   ├── _footer.scss          # Footer styles
│   ├── _header.scss          # Header styles
│   ├── _grid.scss            # Grid system
│   └── _navigation.scss      # Navigation styles
├── pages/
│   ├── _index.scss           # Forwarding all page styles
│   ├── _about.scss           # About page styles
│   ├── _contact.scss         # Contact page styles
│   └── _home.scss            # Home page styles
├── utils/
│   ├── _index.scss           # Forwarding all utility styles
│   ├── _color-utils.scss     # Color manipulation utilities
│   ├── _container.scss       # Container utilities
│   ├── _flow.scss            # Spacing utilities
│   └── _helpers.scss         # Utility classes (e.g., visually hidden)
├── vendors/
│   ├── _index.scss           # Forwarding all vendor styles
│   ├── _bootstrap.scss       # Bootstrap framework styles
│   └── _normalize.scss       # Normalize.css styles
└── styles.scss                  # Main SCSS file
```

### Usage Instructions for `@forward`

The `@forward` directive in SCSS is used to re-export styles from one module to another. This is particularly useful in the `_index.scss` files for organizing and managing styles across your project.

**In each `_index.scss` file**, use `@forward` to include the styles from the other SCSS files in that folder. For example, in `abstracts/_index.scss`:

   ```scss
   @forward 'breakpoints';
   @forward 'colors';
   @forward 'functions';
   @forward 'mixins';
   @forward 'type';
   @forward 'vars';
   ```

**For any additional folder**, create an `_index.scss` file and follow the same pattern to forward the styles. For instance, if you create a new folder called `themes`, you would add:

   ```scss
   // themes/_index.scss
   @forward 'theme-light';
   @forward 'theme-dark';
   ```

### Usage Instructions for `@use`

To use the styles defined in these files, include them in your SCSS files using the `@use` directive. For example, to use all styles from a file or to assign a specific namespace:

```scss
@use 'abstracts/index' as *;  // Makes all styles available without a prefix

@use 'components/buttons' as btn; // Use btn for accessing styles from buttons
```

With this approach, you can use the styles like so:

```scss
.button {
  @include btn.button; // Using a mixin from buttons
}

.some-class {
  color: abstracts.$primary-color; // Accessing a variable from abstracts
}
``` 

This pattern allows you to easily forward and manage your styles while maintaining modularity and clarity throughout your project.

## Usage

To use this SCSS structure in your project:

1. Clone the repository.
```
git clone https://github.com/Beegood-b/sass-7-1-architecture
```
2. Compile your SCSS files into a single CSS file using your preferred Sass compiler (e.g., node-sass, Dart Sass).

This modular structure allows for easy customization and scalability as your project grows.

## Contributing

Feel free to open issues or submit pull requests if you have suggestions for improvements.

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the [MIT License](https://github.com/Beegood-b/sass-7-1-architecture/blob/main/LICENSE).

## Author

**Artjoms Bugajenkovs**  
You can reach me at [Github](https://github.com/Beegood-b).
