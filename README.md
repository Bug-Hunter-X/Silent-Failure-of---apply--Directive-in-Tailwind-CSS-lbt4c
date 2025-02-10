# Silent Failure of @apply Directive in Tailwind CSS

This repository demonstrates a subtle bug in Tailwind CSS related to the `@apply` directive.  When a class name used with `@apply` is misspelled or missing from Tailwind's configuration, there's no clear error message; the styles simply don't apply.

## Bug Description
The `@apply` directive is a powerful feature, but it can be tricky to debug when encountering unexpected styling issues.  This bug causes the `@apply` to fail silently. This means no error is thrown, and the developer might spend considerable time debugging other aspects of the code before noticing the actual issue.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe that the text is not centered and has no blue background, even though these styles are intended to be applied using `@apply`.
4. Check `bugSolution.html` to see the correct implementation.

## Solution
The solution is to carefully check your class names in your Tailwind configuration and ensure that they match the names used with `@apply` exactly.  If you are using a linter, enable Tailwind linting to catch these inconsistencies.
