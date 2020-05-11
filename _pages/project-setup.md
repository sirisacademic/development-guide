---
title: Project Setup
---

## Project Setup

While the specific setup for each SIRIS project varies widely, there are certain
elements that should be present in all source code repositories. This document
aims to detail those elements and suggest corresponding tools and resources.

### Source code management

SIRIS projects use Bitbucket/GitHub for source code management, with their repositories
under a [organization](https://bitbucket.org/sirisacademic/).


### Repository Checklist

Below is an aspirational list of configuration and files for a source
code repository. Not all of these elements will apply to every project (e.g.
visual regression tests don't make sense for an API).

1. [Community profile](https://help.github.com/en/github/building-a-strong-community/about-community-profiles-for-public-repositories)
   - `LICENSE.md` {%include components/tag-standard.html %}{%include components/tag-todo.html %}
   - `CONTRIBUTING.md` {%include components/tag-standard.html %}{%include components/tag-todo.html %}
   - `README.md` {%include components/tag-default.html %}{%include components/tag-todo.html %}
1. [`.gitignore`](https://github.com/github/gitignore) (though also consider a [global config](https://help.github.com/articles/ignoring-files/#create-a-global-gitignore))
1. Programming language version specifications (e.g., `.nvmrc`, `runtime.txt`, `Gemfile`)
1. Dependency version descriptions (e.g., `Gemfile`, `Pipfile`, `package.json`)
1. Build scripts
1. Linter setup (e.g., [`flake8`](http://flake8.pycqa.org/en/latest/),
   [`rubocop`](../ruby/.rubocop.yml),
   [`eslint`](https://github.com/airbnb/javascript/blob/master/linters/.eslintrc) {%include components/tag-suggestion.html %})
1. Docker {%include components/tag-suggestion.html %}
   - Dockerfiles
   - [Compose](https://docs.docker.com/compose/) files
   - [.dockerignore](https://docs.docker.com/engine/reference/builder/#dockerignore-file)
1. Deploy scripts

### Project Management Tool
 
Every project, no matter the size, should use a project management tool to keep
track of ongoing tasks and to do items. The project management tool should be
linked to somewhere in the project's GitHub repository so that others can find
it easily.

- [GitHub Issues](https://guides.github.com/features/issues/) {%include components/tag-default.html%}


### Dependency management

Applications require specific versions of programming languages, libraries,
databases, services, and configuration to execute. A dependency management
solution helps abstract that complexity and makes it easier for cross-functional
teams to create consistent, reproducible, local development environments.

- [Docker](https://www.docker.com/why-docker) {%include components/tag-suggestion.html %}<br>
  See our [Docker for development](./docker/) recommendations.

