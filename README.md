# Eslint config code complexity

Eslint config for adding code complexity constraints to code linting. Let's make code comfort to read and maintain. Config inspired by [Nikita Sobolev's](https://github.com/sobolevn) [talk about code complexity](https://www.youtube.com/watch?v=7EJ5_ONxoyg).

## Usage

1. Add dev dependency:

`npm install --save-dev eslint-config-code-complexity`

or

`yarn add -D eslint-config-code-complexity`

2. Add config extending in eslint config file (e.g. `.eslintrc.json`):

```
...
"extends": ["eslint-config-code-complexity"],
...
```

## Rules description

- **complexity** — Cyclomatic complexity measures the number of linearly independent paths through a program's source code. Complexity setted to 5 as maximum or error.
- **max-params** — Functions that take numerous parameters can be difficult to read and write because it requires the memorization of what each parameter is, its type, and the order they should appear in. As a result, many coders adhere to a convention that caps the number of parameters a function can take. This rule setted to 4 as maximum or error.
- **max-statements** — this rule specify the maximum number of statements allowed in a function. Setted to 7 as maximum or error.
- **max-statements-per-line** — A line of code containing too many statements can be difficult to read. Code is generally read from the top down, especially when scanning, so limiting the number of statements allowed on a single line can be very beneficial for readability and maintainability. This rule setted to 2 as maximum or error.
- **max-nested-callbacks** — Many JavaScript libraries use the callback pattern to manage asynchronous operations. A program of any complexity will most likely need to manage several asynchronous operations at various levels of concurrency. A common pitfall that is easy to fall into is nesting callbacks, which makes code more difficult to read the deeper the callbacks are nested. Setted to 2 as maximum or error.
- **max-depth** — Many developers consider code difficult to read if blocks are nested beyond a certain depth. This rule setted to 3 as maximum or error.
- **max-lines** — Some people consider large files a code smell. Large files tend to do a lot of things and can make it hard following what's going. While there is not an objective maximum number of lines considered acceptable in a file, most people would agree it should not be in the thousands. Recommendations usually range from 100 to 500 lines. This rule setted to 150 as maximum or error.
