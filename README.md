# Deno npm dependency install bug

The npm compatibility layer doesn't symlink npm dependencies local to a package. Since we deno uses a flat directory structure these are then not found.

## Steps to reproduce

1. Clone repository
2. Run `deno run -A index.js`

## Actual outcome

```sh
error: Uncaught Error: Cannot find module 'get-intrinsic'
```

## Expected outcome

It should not error.
