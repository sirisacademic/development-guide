# SIRIS Academic Engineering Practices


This repo is where the SIRIS Academic R+D keeps its guide to best practices and resources for software development. Documentation is written using [Markdown](https://kramdown.gettalong.org/quickref.html) syntax and published as HTML using the [Jekyll](https://jekyllrb.com) static site generator.

The guide has been cloned from the excelent [engineering guides from 18f.gov](https://github.com/18F/development-guide)

## Quicklinks

- Published guide: [pending](https://engineering.sirisacademic.com)
- Raw content: [_pages](_pages)
- [CONTRIBUTING.md](CONTRIBUTING.md) on how to build this guide locally and submitting PRs/issues.

## Aims
This guide is aimed to:
- Support the continuous learning necessary for successful software engineering work.
- Provide SIRIS members with easy-to-understand, actionable guidance around software engineering best practices.
- Promote a central knowledge base of shared tools, common patterns, tutorials, and exemplary source code repositories, to help build technical capacity at our partner agencies so that they might better govern their software development efforts.
- Create a robust and supportive internal environment so that we can, in turn, bolster healthy external communities related to our work.

## How to track what we're doing, and how you can be involved!

We use issues in this repo to track work. If you'd like to suggest a new topic or flag an issue, please [file an issue](https://https://github.com/sirisacademic/development-guide/issues/new/).

The software development industry is ever-changing, and our guide is a living document. Please suggest edits or changes via pull request.

## Development

To run the site locally, we recommend using:
- [`git`](https://git-scm.com)
- `docker` and `docker-compose` (included in [Docker Desktop](https://www.docker.com/products/docker-desktop))

1. Clone the repository:

   ```sh
   git clone https://github.com/sirisacademic/development-guide
   ```
1. From within the repository directory, run:

   ```sh
   docker-compose up --build
   ```

1. Open http://localhost:4000

## Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright
> and related rights in the work worldwide are waived through the [CC0 1.0
> Universal public domain
> dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0
>dedication. By submitting a pull request, you are agreeing to comply
>with this waiver of copyright interest.
