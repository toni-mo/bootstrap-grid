# Bootstrap Grid
**It's a feature of Bootstrap Framework that helps to create a layout for your website.**

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
  
**CDN link to reamote file**
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

![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/contents.png)

## Grid System
Grid - the feature of Bootstrap that helps you create layout. It is series of rows and columns that are represented by css classes. Bootstrap grid has 12 columns.

### Three main CSS classes to create grid
* .container
* .row
* .col

**.container** class is basically general container for whole grid system, for rows and columns. It’s purpose is to center content, give some horizontal padding to it.

**.row** class serves as wrapper for columns. It’s the place to put your columns in.

**.col** class is the place where your content would go.

### Try this simple example
Class **.container** holds everything and creates those margins on the sides. **.row** contains columns. And **.col** is a column for your content. Class **.border** is a Bootstrap utility class that helps us see the border of a column. Our custom class **.height** is just for the purpose of giving visual height to our column.
  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" integrity="sha384-9gVQ4dYFwwWSjIDZnLEWnxCjeSWFphJiwGPXr1jddIhOegiu1FwO5qRGvFXOdJZ4" crossorigin="anonymous">
    <style>
        .height{
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col border">
                <h1>This is column with class .col</h1>
            </div>
        </div>
    </div>
</body>
</html>
```

### Different size of columns
In Bootstrap, Grid is divided into **12** columns. Therefore it provides you with classes for different size columns from **.col-1** to **.col-12**.

.col-1|.col-2|.col-3|.col-4|.col-5|.col-6|.col-7|.col-8|.col-9|.col-10|.col-11|.col-12|
------|------|------|------|------|------|------|------|------|------|------|------|
8.3%|16.6%|25%|33.3%|41.6%|50%|58.3%|66.6%|75%|83.3%|91.6%|100%|

### Using columns with different sizes 
Try replacing `<div class="col">`, from previous example, for the two divs with classes **.col-6**:

```html
<div class="col-6 border height">
  <h1>This is column with class .col-6</h1>
</div>
<div class="col-6 border height">
    <h1>This is column with class .col-6</h1>
</div>
```

### Nested Columns
You can create nested columns. **Each can be divided into 12 smaller columns**. To nest your content with the default grid, add a new **.row** and set of **.col** columns within an existing **.col** column. Nested rows should include a set of columns that add up to 12 or fewer (it is not required that you use all 12 available columns). The following table provides you with example of possible nesting.

Parent Column|.col-12|.col-12|.col-12|.col-10|.col-6
------|------|------|------|------|------|
Child Columns|.col-6 .col-6|.col-8 .col4|.col-3 .col-3 .col-3 .col-3|.col-8 .col-4|.col-6 .col-6|

### Example
Replace two columns with **.col-6**, from previous example, for one **.col-12** column with two child columns with **.col-6**, following code:

```html
<div class="col-12 border">
  Parent column: .col-12
  <div class="row">
      <div class="col-6 border height">
          <h1>Child column: .col-6</h1>
      </div>
      <div class="col-6 border height">
          <h1>Child column: .col-6</h1>
      </div>
  </div>
</div>
```
## Breaking down Grid
All modern websites are using grid for their layout. At first glance it's not that obvious how it works. To get clear understanding, lets break down the grid of **youtube** page and try to recreate it in the following few sections.

## Webpage itself
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/youtube-screenshot.png)

## Webpage with grid above
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-whole-system.png)

## Recreating the grid
Lets take a look at the following wireframe and try to create it with code.

## Creating container
Start by creating **html base** document with **CDN link** for **Bootstrap**. And adding **div with .container class** to it.
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
