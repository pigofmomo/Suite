# Coding Standards for R

We will follow the https://style.tidyverse.org/ style guide to benefit from two R packages supporting this style guide:

- [styler](http://styler.r-lib.org/)
- [lintr](https://github.com/jimhester/lintr)

This coding standards will outline the more important aspects of the aforementioned style.

# RStudio IDE Settings

- Identation of 2
- Use spaces instead of tabs

# Naming Convention

Use meaningful and understandable names. Code should read as a story and only some well known abbreviations such as pk etc. should be used

## Files

- Underscores separated for multiple words
- All lower case
- Ends in .R

```
# Good
fit_models.R
utility_functions.R

# Bad
fit models.R
foo.r
stuff.r
```

## Object names

- Variable and function names should use only lowercase letters, numbers, and _. Use underscores (_) (so called **snake case**) to separate words within a name.

- Class names on the other hand should use **Pascal Casing**

- True constant variables should use **ALL_CAPS Casing**

```
- Class name: `Parameter`
- Variable name: `parameter_to_delete`
- Method and function name: `perform_simulation`
- Constant variable: `DEFAULT_PERCENTILE <- 0.5

```

- Do not use Hungarian notation (e.g. g for global, b for boolean, s for strings etc...)

## Functions

Only use `return()` for early returns. Otherwise, rely on R to return the result of the last evaluated expression.

## Comments

- Do not comment the obvious
- Use comments to explain the “why” not the “what” or “how”.
- Indent comment at the same level of indentation as the code you are documenting
- All comments must be written in English
- Do not generate commments automatically
- Do comment algorithm specifics. For example why would you start a loop at index 1 and not at 0 etc...
- If a lot of comments are required to make a method easier to understand, break down the method in smaller methods
- Really, do not comment the obvious

# Syntax

## Spacing

Use the `styler` plugin. It will style the file for you. Otherwise see [here](https://style.tidyverse.org/syntax.html#spacing)

## Global Variables

- Except for program constants or trully global states, never use global variables. If a global object is required, this should be absolutely discussed in team.

- No hard coded strings and magic number should be used. Declare a constant instead

## Style

### Long Lines

Strive to limit your code to 80 characters per line

### Assignments

Use `<-`, not `=`, for assignment.

### Semicolons

Don’t put `;` at the end of a line, and don’t use `;` to put multiple commands on one line.

**Note:** All these styling issues, and much more, are corrected automatically with `styler`

### Code blocks

- `{` should be the last character on the line. Related code (e.g., an if clause, a function declaration, a trailing comma, …) must be on the same line as the opening brace.

- The contents should be indented

- `}` should be the first character on the line.

- It is s ok to drop the curly braces for very simple statements that fit on one line, **as long as they don’t have side-effects**.

```
# Good
y <- 10
x <- if (y < 20) "Too low" else "Too high"

# Bad
if (y < 0) stop("Y is negative")

if (y < 0)
  stop("Y is negative")

find_abs <- function(x) {
  if (x > 0) return(x)
  x * -1
}
```

# Tests

Refer to chapter [Tests](https://style.tidyverse.org/tests.html)

# Error messages

Refer to chapter [Errors](https://style.tidyverse.org/error-messages.html)