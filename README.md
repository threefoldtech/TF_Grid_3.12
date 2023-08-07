# TF_Grid_3.12
Documentation of the TF Grid 3.12 release, including improved tokenomics and better defined governance. Please see the issues for ongoing discussions, or open a new one with your comments and suggestions.

## Serve locally

You can build and serve the book locally, to view changes in a web browser.

### Requirements

- Make
- [mdbook](https://rust-lang.github.io/mdBook/guide/installation.html)
- [mdbook-mermaid](https://github.com/badboy/mdbook-mermaid)

### build

`make build`

### Serve

`make serve`
will open the browser  

## Adding pages

To add new pages to this book, follow these steps:

1. Add the md file to [src](./src) directory.
2. Add the path of the md file to [SUMMARY](./src/SUMMARY.md).
3. Then use `make build` and `make serve` to see your changes on the browser.
