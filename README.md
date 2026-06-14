# GOV.SA Design System
Design System is a guide that includes the designing process and is created to ensure that the user gets the best experience when using the GOV.SA platform and channels and helps designers and developers work together in a regular manner.

## CSS architecture

- GOV.SA is built on [Bootstrap](https://getbootstrap.com).
- The CSS foundation of GOV.SA is built with the Sass language.
- GOV.SA built mobile first.
- CSS selectors are prefixed with GOV.SA (For example: .govsa-button). This identifier helps the design system avoid conflicts with other styles on a site which are not part of GOV.SA design system.
- Uses a [BEM](http://getbem.com/introduction/) approach for naming CSS selectors. Blocks are separated from elements with two underscores (__) For example: .govsa-button__elem.  Modifier classes consist of the base class plus a modifier suffix, separated by two dashes (--) for example: govsa-button--disabled , govsa-button__secondary--disabled.

**CSS and SCSS File Organization:**
```bash
GOV.SA-design-system/ 
 ├── css/ 
 │   ├── govsa-ds.min.css.map  
 │   ├── govsa-ds.min.css
 │   └── govsa-ds.css  
 ├── scss/ 
 │   ├── components/
 │   │   ├── accordion/
 │   │   ├── alert/
 │   │   ├── breadcrumb/
 │   │   ├── button/
 │   │   ├── card/
 │   │   ├── checkbox/
 │   │   ├── color/
 │   │   ├── dropdown/
 │   │   ├── file-upload/
 │   │   ├── footer/
 │   │   ├── header/
 │   │   ├── image/
 │   │   ├── link/
 │   │   ├── outlin/
 │   │   ├── pagination/
 │   │   ├── radio/
 │   │   ├── search/
 │   │   ├── side-navigation/
 │   │   ├── switch/
 │   │   ├── table/ 
 │   │   ├── tabs/
 │   │   ├── tag/
 │   │   ├── text-input/

```
## JavaScript Organization:
```bash
├── js/
│   ├── file-upload.js 
│   ├── header.js 
│   ├── search.js 
│   ├── side-navigation.js 
│   ├── tag.js 
│   ├── govsa-ds.js 
│
```


## Installation:
How to you use the GOV.SA design system depends on the needs of your project.

You have two options to get the design system:
-   [Download the design system](#download-the-design-system) if you are not familiar with npm and package management.
-   [Use the design system npm package](#install-using-npm) if you are familiar with using npm and package management.

We recommend that you install GOV.SA design system using npm because it is easier way to be installed and updated and you will be able to select individual SCSS and JS of GOV.SA design system.

## Download the design system: 
1.  Download the GOV.SA-ds zip file from the latest GOV.SA-ds release and open that file.

After extracting the zip file you should see the following file and folder structure:
```bash
GOV.SA-design-system/
├── css/
│   ├── govsa-ds.min.css.map
│   ├── govsa-ds.min.css
│   └── govsa-ds.css
├── fonts/
├── img/
├── js/
│   ├── govsa-ds.min.js.map
│   ├── govsa-ds.min.js
│   └── govsa-ds.js
└── scss/
```
2.  Copy the GOV.SA-design-system folder into a relevant place in your project’s code base.

 Here is an example structure for how this might look:

```bash
  example-project/
├── assets/
│   ├── GOV.SA-design-system
│   ├── stylesheets/
│   ├── images/
│   └── javascript/
└── index.html
```
3.  Reference the CSS and JavaScript files in each HTML page We also provide Sass files in the zip package which you can use to generate new CSS. 

 **Here is an example of how to reference these assets in your index.html file:**

**Note**: if you are going to use Arabic language, kindly change the language to “ar” and        direction to “rtl” in the body.

```bash
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <title>My Example Project</title>
    <link rel="stylesheet" 
    href="assets/Gov.sa-design-system/css/govsa-ds.min.css" />
  </head>
  <body lang="en" dirc= "tr">
    <script src="assets/ Gov.sa-design-system /js/govsa-ds.min.js"></script>
  </body>
</html>
```
And that’s it :)

# Install using npm:
1.  Install Node and npm.
2.  Create a package.json file if you don’t already have one. You can create a default package.json file by running npm init from the root of your project. 
3.  Install GOV.SA design system in your project  Npm install govsa-ds.
Now, the GOV.SA design system package installed as a dependency.

**GOV.SA design system folder structure:**

```bash
node_modules/govsa-ds/
├── dist/
│   ├── css/
│   ├── fonts/
│   ├── img/
│   ├── js/
│
├──fonts/
│
├──govsa-icons/
│
├──images/
│
├──js
│
├──Scss/
│
├──typography/
│
├── theme/
│
├── packages/ 
│
├──index.html
```
**Note**: We do not recommend directly editing the design system files in node_modules.

## Using the GOV.SA design system package:
If you want to take full advantage of GOV.SA design system custom settings and add build new styles and components with the GOV.SA design system toolset, you’ll need a way to access the assets in the GOV.SA design system package and compile custom CSS from the GOV.SA design system source files.
Use the task manager [Gulp](https://gulpjs.com/) as a way to add GOV.SA design system assets to a project and compile our CSS from the package source.
Go to [GOV.SA-gulp](https://github.com/GOV-SA/Gulp) repo to see more details.

**Import Styles:**

```bash
scss/
├── theme/
│   ├── govsa-theme-required.scss 
│   ├── govsa-theme-global.scss 
│
├──packges/
│   ├── govsa-accordion.scss
│   ├── govsa-alert.scss
│   ├── govsa-breadcrumb.scss
│   ├── govsa-button.scss
│   ├── govsa-card.scss
│   ├── govsa-checkbox.scss
│   ├── govsa-dropdown.scss
│   ├── govsa-header.scss
│   ├── govsa-footer.scss
│   ├── govsa-file-upload.scss
│   ├── govsa-icons.scss
│   ├── govsa-image.scss
│   ├── govsa-link.scss
│   ├── govsa-outlin.scss
│   ├── govsa-pagniation.scss
│   ├── govsa-radio.scss
│   ├── govsa-search.scss
│   ├── govsa-sid-navigation.scss
│   ├── govsa-switch.scss
│   ├── govsa-table.scss
│   ├── govsa-tabs.scss
│   ├── govsa-tage.scss
│   ├── govsa-text-input.scss

```
- govsa-theme-required.scss: include the required theme (color, font)
- govsa-theme-global.scss: include all design system

**you have two way to import govsa-ds:**

if you want to import all govsa-ds add the below to your Sass file:
```bash
@import " govsa-ds "
```
if you want to import individual component (for example a button), add the below to your Sass file:
```bash
@import "node_modules/govsa-ds/theme/govsa-theme-required.scss"
@import "node_modules/govsa-ds/packages/govsa-button.scss"
```
**Note:** if you are going to use Arabic language, kindly change the language to “ar” and direction to “rtl” in the body.

**Import JavaScript:**

JavaScript architecture:
```bash
├── js/
│   ├── file-upload.js
│   ├── header.js  
│   ├── search.js 
│   ├── side-navigation.js 
│   ├── tag.js 
│   ├── govsa-ds.js 
│
```
- file-upload.js: if you are going to use file upload, you will need to import file-upload.js in 
- search.js: if you are going to use search, you will need to import search.js
- side-navigation.js: if you are going to use side navigation, you will need to import side-navigation
-   tag.js: if you are going to use tag, you will need to import tag.js
- govsa-ds.js: include the all JavaScript file.


## Installation the design system project
1. Clone the project
2. Go to the project root directory
3. Run `yarn`

## Running on development using [dev server](https://github.com/webpack/webpack-dev-server)

Run `yarn  start:dev` to start to webpack dev server with HMR ready

## For production 

Run `yarn  build` to build project's all assets in `dist` folder.
<!-- trigger rebuild -->
