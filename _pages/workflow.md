---
title: Workflow Best Practices
---

# Workflow Best Practices

Project teams may vary, but across SIRIS engineering we aim for consistency
around deployments, git etiquette, and similar workflow conventions.

## Continuous Integration & Deployment

### Standards
{%include components/tag-todo.html %}

## Git & Bitbucket/GitHub

Git is our version control system of choice and Bitbucket (mainly) and GitHub our current
repository platforms, but how to use these tools can be spelled out in a bit
more detail. Note that we are looking to consolidate this with our existing
documentation on [code review]({{site.baseurl}}/code-review) and [example
workflows]({{site.baseurl}}/example-workflows).

Most of our source is hosted at:

1. [Bitbucket SIRIS Academic account](https://bitbucket.org/sirisacademic/) since it's client-based. 
2. For those developments that can be exposed publicly or open sourced, we have an account at [Github SIRIS Academic page](https://github.com/sirisacademic).



### Defaults

- Generally we prefer **branches** over forks to ease internal collaboration.
  If your project has many outside contributors, consider forks instead.
- When in doubt, use feature branches and **gitflow** as
  your branch naming scheme. Good guidelines about how to use gitflow, [here](http://nvie.com/posts/a-successful-git-branching-model/) and [here](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow).
  ![Plot1]({{site.baseurl}}/workflow/gitflow.svg)
- Keep your repository **clean**; delete merged branches and avoid committing
  files specific to your dev environment (e.g. `.DS_Store`).
- Whether you are using bitbucket or github, use the issue tracker to manage the features/issues within the project. Ideally, each issue should hold a specific development/feature and a branch should be created to tackle the issue. There are dozens of naming policies for the branches, so just keep some logic when naming ('issue-whatever-i-am-doing', 'feature-new-component').
- Follow [this
  guidance](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
  about **good commit messages**.