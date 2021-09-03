# Sass Utils

This package Sass utility for small projects. That contains functions, mixins, and variables.

## Usage

Copy `sass-utils` directory to the particular directory of your project.

```
main.scss
sass-utils/
|- __all.scss
|- functions/
|- mixins/
|- variables/
```

Then import `__all.scss` that forwards all of the utility functions, mixins and variables. Loading that, use `@use` directive by the first line of your scss file.

```scss
@use './sass-utils/_all' as *;
```

If you want to use the utilities without a prefix, write `as *` after the file path.

### How to refer variables

When you want to refer a variable, you should call a function that get a variable, because all the variables in the package are declared in `map` type. For example, code as follow.

```scss
h2 {
  font-size: get-font-size(lg);
}
```

