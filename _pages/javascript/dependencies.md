---
title: Dependencies
sidenav: js
---
# Dependencies
The word "dependency" refers to all of the frameworks, libraries, and other tools that your project relies on. *Dependency management* is the process by which tools are incorporated into your project, removed and updated (for instance, when you need a new version of [jQuery]). Here are the tools that we recommend for managing dependencies:

## Bower
{%include components/tag-standard.html %} __Do not use Bower.__

It's not needed and should be phased out and replaced by npm. More information can be found here: [Why We Should Stop Using Bower – And How to Do It](http://gofore.com/ohjelmistokehitys/stop-using-bower/).

Have in mind although that some of the projects developed in the past could still be relying on Bower since they are not updated.

## npm
{%include components/tag-default.html %} [npm] informally stands for *N*ode *P*ackage *M*anager, and is the package manager node uses. Its usage is very similar to Bower because the latter was inspired by the former.

### npm instructions
1. Get [Node.js].
2. To initialize your project, run `npm init` in your project directory, which will create a `package.json`.
3. Install some dependencies with `npm install --save [name]`, e.g.
  - [jQuery]: `npm install --save jquery`
  - [D3]: `npm install --save d3@v3.5.5` (version 3.5.5)

npm installs its dependencies in the `node_modules` directory. Common conventions dictate that `node_modules` should be excluded from source control by adding it to your project's `.gitignore`, primarily because Node.js-friendly environments  recognize the existence of `package.json` and automatically install dependencies as needed.

### Install npm

We recommend that developers (note 1) install both node and npm through a tool called nvm. nvm (which stands for Node version manager) is a software that allows you to run multiple versions of node in different projects on the same computer. Its benefits include

- Installs npm in a manner that doesn't require running sudo to install global packages.
- Easily be able to switch between multiple node versions with a project configuration file or command.

To install on MacOSX or linux, follow the instructions on the [nvm site](https://github.com/creationix/nvm#installation). If you system has a c++ compiler setup, you'll likely be able to install it with this simple script:

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.6/install.sh | bash
```



### Publishing
#### Scoping a package to the 18F npm org
{%include components/tag-todo.html %} Content is here, need to implement what is described below:
SIRIS has an npm organization called [SIRIS Academic](https://www.npmjs.com/org/sirisacademic) that is meant to organize permissions and packages related to SIRIS. As an SIRIS developer, when publishing a package, you have the choice whether to scope a package to the SIRIS org or not. Scoped packages will always be prefixed with `@sirisacademic/` before their package name and can have their permissions managed by people in the org. More information about scoped packages can be found on the [npm documentation](https://docs.npmjs.com/misc/scope).

##### Guidance on when to scope a package or not
- A package *should not* be scoped to SIRIS Academic if it is not necessary for consumers of the package to be aware of SIRIS Academic in order to use it.
- A package *should* be scoped to SIRIS if its use cases fall mainly inside of SIRIS.
  - Example: [@sirisacademic/stylelint-rules](https://github.com/sirisacademic/stylelint-rules) is scoped to SIRIS because it's an SIRIS Academic specific linting configuration that's directly linked to the SIRIS guides site.
- A package *should* be scoped to SIRIS to avoid naming conflicts.
  - Example: If SIRIS made a generic front-end accordion to use across SIRIS sites, it should probably be scoped to `@sirisacademic/accordion` to avoid conflicts with all other accordions out there.

##### How to scope a package to SIRIS Academic
- Ensure you are part of the SIRIS Academic npm org and have at least developer rights. This can be found on the [SIRIS Academic org team page](https://www.npmjs.com/org/sirisacademic/members).
  - If you don't have the proper access, ask an admin to add you.
- If the package has not been published to SIRIS Acadmeic yet, follow the [instructions on npm](https://docs.npmjs.com/getting-started/scoped-packages) for scoped packages.
- If the package has already been published, it currently cannot be scoped, so may need to be renamed. See the [npm documentation on existing packages](https://docs.npmjs.com/orgs/preexisting-packages) for more information.

##### General tips for publishing
- Use [semver](http://semver.org/).
- Include instructions on how to use the modules in the README.md. Start from `npm install`, as this is generally a convention on npm.
- Test to ensure that your package works with any required versions of node and works on Windows.

### Node and the browser
Using [Node.js] modules in the browser can be either straightforward or convoluted, depending on the project. Some project packages come with browser-ready `.js` files, whereas others require build tools such as [Browserify] or [Webpack] to translate some Node-specific JavaScript so that it can be run in browsers. Visit the #javascript channel on Slack if you need help with these tools.

## Yarn
{%include components/tag-todo.html %}
Add content similar to the npm block

## Manual dependency management
Many dependencies consist of a single file and can be more easily incorporated simply by copying them into your project. We have some recommendations for how this should be done:

1. Establish a specific directory for 3rd-party assets, e.g. `js/vendor` for JavaScript or `assets/vendor` for frameworks that consist of CSS, images and/or JavaScript.
2. Download the assets to this directory, e.g. in your terminal:

  ```sh
  cd js/vendor
  curl -O http://code.jquery.com/jquery.min.js
  ```