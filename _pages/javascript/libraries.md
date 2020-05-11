---
title: Libraries
sidenav: js
---
# Libraries

Libraries used in front-end development are mainly scoped into 3 categories: Data Visualization, Data utilities, and utility libraries.

## Data Visualization

### D3
{%include components/tag-default.html %}
[D3](https://d3js.org/) is a JavaScript library for manipulating documents based on data. D3 helps you bring data to life using HTML, SVG, and CSS. D3’s emphasis on web standards gives you the full capabilities of modern browsers without tying yourself to a proprietary framework, combining powerful visualization components and a data-driven approach to DOM manipulation.

### Vega
{%include components/tag-default.html %}
[Vega](https://vega.github.io/vega/) is a visualization grammar, a declarative language for creating, saving, and sharing interactive visualization designs. With Vega, you can describe the visual appearance and interactive behavior of a visualization in a JSON format, and generate web-based views using Canvas or SVG.

**Since Vega does not use the programmatic approach of D3, it is recommended over D3**. Sharing Vega specification with other members of the team is a much more efficient way to reuse visualizations, due to:
- The logic behind the visualization is always tied to a visualization grammar, there is no source code (a consuming task when is not yours) to be understood.
- The Vega project offers an ecosystem of usable and interoperable tools. Check [here](https://vega.github.io/vega/about/projects/) to see a list of high-level tools.



## Data Analysis

### Datalib
{%include components/tag-suggestion.html %}
[Datalib](https://github.com/vega/datalib) is a JavaScript data utility library. It provides facilities for data loading, type inference, common statistics, and string templates. While datalib was created to power [Vega](https://vega.github.io/vega/) and related projects, it is also a standalone library useful for data-driven JavaScript applications on both the client (web browser) and server (e.g., node.js).

## Utilities

### Lodash
{%include components/tag-default.html %}
A modern JavaScript utility library delivering modularity, performance & extras.
Lodash makes JavaScript easier by taking the hassle out of working with arrays, numbers, objects, strings, etc.
Lodash’s modular methods are great for:
- Iterating arrays, objects, & strings
- Manipulating & testing values
- Creating composite functions

In order to improve readability when performing manipulations, it is suggested to use 
always function chaining:
```
var users = [
  { 'user': 'barney',  'age': 36 },
  { 'user': 'fred',    'age': 40 },
  { 'user': 'pebbles', 'age': 1 }
];
 
var youngest = _
  .chain(users)
  .sortBy('age')
  .map(function(o) {
    return o.user + ' is ' + o.age;
  })
  .head()
  .value();
// => 'pebbles is 1'
```