# Bootstrap Grid
**It's an easy way to create layout for your website.**

_(layout - the way in which the parts of something are arranged or laid out.)_


## Bootstrap
Bootstrap is a free and open-source front-end library for designing websites and web applications. It contains HTML- and CSS-based design templates for typography, forms, buttons, navigation and other interface components, as well as optional JavaScript extensions. Unlike many web frameworks, it concerns itself with front-end development only.

**CSS Framework = CSS Library = CSS file**

[Bootstrap](https://getbootstrap.com/)


## What are the pros of Bootstrap?
* Grid system.
* Prepared styles for different html elements.
* Ready components: navigation, modal windows, carousel.
* Prepared solutions for getting things done quickly.
* Good starting point in learning how modern websites are built.

## How to get started?

  * [CDN](https://getbootstrap.com/docs/4.1/getting-started/introduction/#css) _(Content Delivery Network)_ - copy and paste link into `<head></head>` section.

  * [Download](https://getbootstrap.com/docs/4.1/getting-started/download/#compiled-css-and-js) bootstrap archive with css and js files on your computer, in the `<head></head>` create link that refers to **bootstrap.css** file. When you're downloading manualy you have two options. You can:
    * use whole bootstrap with all it's features.
    * use only grid feature.
  
**CDN link**
```html
<head>
    <title>Document</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" integrity="sha384-9gVQ4dYFwwWSjIDZnLEWnxCjeSWFphJiwGPXr1jddIhOegiu1FwO5qRGvFXOdJZ4" crossorigin="anonymous">
</headsup>
```

**Link to file on your machine**
```html
<head>
    <title>Document</title>
    <link rel="stylesheet" href="pathToYourBootstrapFile/bootstrap.css">
</head>
```

### CSS files you get
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/contents.png)

### Grid System
Grid - series of rows and columns that is represented by css classes. Bootstrap grid has 12 columns. Each column can be divided again into 12 columns.

### Three main CSS classes
* .container
* .row
* .col

  * **.container** class is basically general container for whole grid system, for rows and columns. It’s purpose is to center content, give some horizontal padding to it.
  * **.row** class serves as wrapper for columns. It’s the place to put your columns in.
  * **.col** class is the place where your content would go.
  
 ### Different size of columns
.col-1|.col-2|.col-3|.col-4|...|.col-12|
------|------|------|------|---|-------|
8%|12%|16%|24%|...|100%|

### Breaking down Grid
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/youtube-screenshot.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-whole-system.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/whole-system.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/row-row.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/col-col-col.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/col-col-col.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/row.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/4columns.png)
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/whole-system.png)

### Responsiveness
Is your website responsive?
Is it mobile friendly?
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/responsiveness-table.PNG)

### Alignment
 1. Vertical alignment
 2. Horizontal alignment

### Vertical alignment(for row)
Here we have to work with row
 * **.align-items-start**
 * **.align-items-center**
 * **.align-items-end**
 
```html
<div class="row align-items-start">
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
    <div class="col">
      One of three columns
    </div>
  </div>
```
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/vertical-alignment.PNG)

### Vertical alignment(for column)
Here we're working with column
 * **.align-self-start**
 * **.align-self-center**
 * **.align-self-end**
```html
<div class="container">
  <div class="row">
    <div class="col align-self-start">
      One of three columns
    </div>
    <div class="col align-self-center">
      One of three columns
    </div>
    <div class="col align-self-end">
      One of three columns
    </div>
  </div>
</div>
```
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/vertical-alignment-column.PNG)

### Horizontal alignment
Working with row again
 * **.justify-content-start**
 * **.justify-content-center**
 * **.justify-content-end**
 * **.justify-content-around**
 * **.justify-content-between**
 
```html
<div class="row justify-content-start">
    <div class="col-4">
      One of two columns
    </div>
    <div class="col-4">
      One of two columns
    </div>
</div>
```
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/horizontal-alignment.PNG)

### Offsetting
Sometimes we want to have some empty space before between or after columns. Or just move them a little bit.
Move columns to the right using **.offset-md** classes. These classes increase the left margin of a column by * columns. For example, **.offset-md-4** moves .col-md-4 over four columns.

```html
<div class="row">
  <div class="col-md-4">.col-md-4</div>
  <div class="col-md-4 offset-md-4">.col-md-4 .offset-md-4</div>
</div>
<div class="row">
  <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
  <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
</div>
<div class="row">
  <div class="col-md-6 offset-md-3">.col-md-6 .offset-md-3</div>
</div>
```

![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/offsetting.PNG)

### Proper semantic
Don't use **Grid classes** just with `<div>`'s, try to place them inside proper semantic blocks.
For example use class **.container** as child of such elements: `<header></header>`, `<main></main>`, `<footer></footer>`.
```html
<body>
    <header>
        <div class="container">
            <div class="col-12"></div>
        </div>
    </header>
    <main>
        <div class="container">
            <div class="row">
                <div class="col-8"></div>
                <div class="col-4"></div>
            </div>
        </div>
    </main>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-6"></div>
                <div class="col-6"></div>
            </div>
        </div>
    </footer>
</body>
```

### Summary, Bootstrap Grid
 1. Easy to use, 3 main classes.
 2. Differen size columns.
 3. Responsive, mobile friendly.
 4. Alignment and offsetting.
 
### Useful Links
 * [Bootstrap documentation](https://getbootstrap.com/)
 * [Bootstrap Grid](https://getbootstrap.com/docs/4.1/layout/grid/)
 * [W3School guide about Bootstrap Grid](https://www.w3schools.com/bootstrap/bootstrap_grid_system.asp)
 
# Thank you!
