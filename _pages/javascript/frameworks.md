---
title: Frameworks
sidenav: js
---
# Frameworks
## Angular
{%include components/tag-suggestion.html %}
AngularJS (commonly referred to as "Angular") is an open-source web application framework maintained by Google and by a community of individual developers and corporations to address many of the challenges encountered in developing single-page applications ([Wikipedia](http://en.wikipedia.org/wiki/AngularJS)).

#### When to use:
- Sites with heavy front end, JavaScript UI interactions (single page apps) such as:
  - creating, updating, deleting of information without a server reload
  - real-time messaging platforms, such as chat or complex messaging such as email
  - complex data visualization dashboards
  - lazy-loaded from the back end
- When the site's design specifies a single page app architecture over classic server request and response.
- When the whole site will be built with Angular to maintain front-end code consistency.

#### When not to use:
- For a single or a few simple components (with the rest of the site not using Angular), instead see React or Web Components.
- Exporting a module that isn't an Angular module.
- If there is a strict requirement that the site should work for users that have JavaScript disabled.
- If there already is an active M**V framework (Backbone, ampersand, Ember) being used on the site.
- When the site's design doesn't benefit from a single page app architecture.
- When the long-term maintenance dev team is very unfamiliar with Angular and don't have the resources to learn or hire for it.

#### Pros:
- Takes care of a lot of boilerplate code for front-end interactions.
- Attempts to extend HTML itself, and was designed so less experienced devs could use it.
- Being maintained and developed by Google generally means good support.

#### Cons:
- While open source, is maintained primarily by Google.
- Has been known to implement breaking changes in major version updates.
- Built with Typescript and Dart, both of which are not ECMA standardized (as opposed to vanilla JS or ES6).
- Has a steep learning curve and is very opinionated, meaning you learn Angular rather than JavaScript.



## React
{%include components/tag-suggestion.html %}
React (sometimes styled React.js or ReactJS) is an open-source JavaScript library for creating user interfaces that aims to address challenges encountered in developing single-page applications ([Wikipedia](https://en.wikipedia.org/wiki/React_(JavaScript_library))).

#### When to use:
- Single page apps that requires data manipulation on the front end without a server side request/response architecture.
- When there's a strong need to render JavaScript based UI on the server due to performance or accessibility reasons.
- JavaScript UI that incorperates many nested components.
- A UI with many components and updates that needs to be performance conscious.
- When only a "view" framework is desired/required.
- To ensure all front-end components conform to a single standard.

#### When not to use:
- When a complex build process is not feasible. React requires transforming "jsx" files to regular JavaScript.
- When developers unfamiliar with JSX and don't have time to learn.
- While open source, is maintained primarily by Facebook.


## Redux
{%include components/tag-suggestion.html %}
Redux is a predictable state container for JavaScript apps.

It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test. On top of that, it provides a great developer experience, such as live code editing combined with a time traveling debugger.

You can use Redux together with React, or with any other view library. It is tiny (2kB, including dependencies), but has a large ecosystem of addons available.

#### When to use:
- A complex JavaScript app that requires both viewing and modifying (CRUD) data
  in a UI rendered on the client. Redux will likely be overkill for apps that
  don't modify data in any way.
- When the data service for the front end is REST and/or something besides REST,
  such as Websockets.
- An app thats data flow has grown or will grow overly complex.

#### When not to use:
- Applications that don't require any updating (create, update, delete) of data.
- When the cost of updating an app's architecture to Redux is more than the cost
  of writing the software as it exists.

#### Pros:
- Predictability and simplicity
- Unidirectional data flow and immutability
- Separation of data and presentation
- Extensibility (via middlewares)
- Popularity and community
- Tooling support
#### Cons:
- Boilerplate (views, action types, action creators, reducers, selectors, …)
- No out-of-the-box solution for dealing with side-effects (available through middlewares such as redux-thunk or redux-saga)
- Actions are disconnected from their effect (which is defined in the reducer)
