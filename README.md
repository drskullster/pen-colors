# Pen Colors

Catalogue of pen colors for plotting.

## What is this?

Creative coders who want to plot their artworks need to approximate their
pen colors on the computer screen to be able to preview their plot (somewhat) accurately.

This project aims to standardize and simplify the process
by having a single source of truth available to everyone in a wide range of formats.

Although the tooling is in Node.js, it is intended to be generic and usable by any system.

## How to use on the web

You can either use the UMD export which adds a `PenColors` object to the global scope, or import the ES module.

* UMD export

```html
<script type="text/javascript" src="https://unpkg.com/pen-colors@1/lib/js/pen-colors.umd.js"></script>
<script type="text/javascript">
console.log(PenColors.stabilo.point88[11].$value); // returns '#a4daf3'
</script>
```

* ES module

```html
<script type="module">
import PenColors from 'https://unpkg.com/pen-colors@1/lib/js/pen-colors.esm.js';
console.log(PenColors.stabilo.point88[11].$value); // returns '#a4daf3'
</script>
```

You can also install the package via npm:

```shell
npm install pen-colors --save
```

then

```js
import PenColors from 'pen-colors';
console.log(PenColors.stabilo.point88[11].$value); // returns '#a4daf3'
```

## I'm not using the web platform

You can download or link to the colors in JSON format: https://unpkg.com/pen-colors@1/lib/json/pen-colors.json

Or if you want an object containing color descriptions: https://unpkg.com/pen-colors@1/lib/json/pen-colors.full.json

If you would like to bundle this project as a library for your language or package manager, please open an issue


## Contribute

Each pen color is represented by a token, defined in JSON files using the [DTCG format](https://www.w3.org/community/design-tokens/).
These tokens are living in the  `src` folder, where each file represents a brand.
The structure of the files should follow the brand naming and categorization.

These files are transformed using [Style Dictionary](https://v4.styledictionary.com/) to different formats,
with the goal of being compatible with most languages and workflows.

Colors are defined as tokens in JSON files in the `src` folder. 

### How to add colors to the repository

#### 1. Create a file if it doesn't exist yet

If the brand you want to add doesn't exist yet, create a JSON file in the `src` folder with the name of the brand.

#### 2. Add color values to the file

The structure and the different categories will depend on the brand and their 
collection, it doesn't have to follow a similar pattern between brands.

#### 3. Commit your changes

This project uses [semantic-release](https://semantic-release.gitbook.io/semantic-release) to automate releases and NPM package publishing.
As such, every commit adding colors should start with `feat:`. This will 
create a new minor version. Example:

```
feat: add colors for stabilo point 88 pens
```

If you want to change the value of existing colors, you can use `fix:`. 
This will create a new patch version. Example:

```
fix: change the color values for some stabilo point 88 pens
```

Any removal or change to the structure of existing colors should be considered a breaking change, thus
bump a new major version to not break user workflows. This is achieved by adding a line 
beginning with `BREAKING CHANGE:` in the commit body.

```
fix: change stabilo naming structure

BREAKING CHANGE: The stabilo structured has been changed.
<Share more information about the change>
```


#### 4. Open a PR

Open a PR with your changes!

## TODO

* Generate a Markdown file listing all available pen colors. 