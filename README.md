# Bootstrap Grid
**It's a feature of Bootstrap Framework that helps to create a layout for your website.**

_(layout - the way in which the parts of something are arranged or laid out.)_

### Summary of content
* [Bootstrap](https://github.com/toni-mo/bootstrap-grid#bootstrap)
* [How to get started](https://github.com/toni-mo/bootstrap-grid#how-to-get-started)
* [Grid System](https://github.com/toni-mo/bootstrap-grid#grid-system)
    * [Different size of columns](https://github.com/toni-mo/bootstrap-grid#different-size-of-columns)
    * [Nested Columns](https://github.com/toni-mo/bootstrap-grid#nested-columns)
* [Breaking down Grid](https://github.com/toni-mo/bootstrap-grid#breaking-down-grid)
* [Responsive Grid](https://github.com/toni-mo/bootstrap-grid#responsiveness)
* [Alignment](https://github.com/toni-mo/bootstrap-grid#alignment)
* [Offsetting](https://github.com/toni-mo/bootstrap-grid#offsetting)
* [Proper Semantic](https://github.com/toni-mo/bootstrap-grid#proper-semantic)
* [Useful links](https://github.com/toni-mo/bootstrap-grid#useful-links)

## Bootstrap

[<-- back to summary](https://github.com/toni-mo/bootstrap-grid#summary-of-content)

Bootstrap is a free and open-source front-end library for designing websites and web applications. It contains HTML- and CSS-based design templates for typography, forms, buttons, navigation and other interface components, as well as optional JavaScript extensions. Unlike many web frameworks, it concerns itself with front-end development only.

**CSS Framework = CSS Library = CSS file**

[Bootstrap](https://getbootstrap.com/)


### What are the pros of Bootstrap?
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
  
**CDN link to remote file**
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
<div class="col-6 border">
  <h1>This is column with class .col-6</h1>
</div>
<div class="col-6 border">
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
      <div class="col-6 border">
          <h1>Child column: .col-6</h1>
      </div>
      <div class="col-6 border">
          <h1>Child column: .col-6</h1>
      </div>
  </div>
</div>
```
## Breaking down Grid
All modern websites are using grid for their layout. At first glance it's not that obvious how it works. To get clear understanding, lets break down the grid of **youtube** page and try to recreate it in the following few sections.

### Webpage itself
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/youtube-screenshot.png)

### Webpage with grid above
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-grid/clear-system.png)

### Recreating the grid
Lets take a look at the following wireframe and try to create it with code.

#### Webpage with container
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-grid/wireframe-container.png)

### Creating container
Start by creating **html base** document with **CDN link** for **Bootstrap**. And adding **div with .container class** to it.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" integrity="sha384-9gVQ4dYFwwWSjIDZnLEWnxCjeSWFphJiwGPXr1jddIhOegiu1FwO5qRGvFXOdJZ4" crossorigin="anonymous">
</head>
<body>
    <div class="container">
        <h1>.container</h1>
    </div>
</body>
</html>
```

#### Webpage with container, and 2 main rows
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-grid/wireframe-2rows.png)

### Adding 2 main rows
Lets add inside **.container** two **divs with class .row**

```html
<div class="container">
    <div class="row"></div>
    <div class="row"></div>
</div>
```

#### Webpage with container, 2 main rows, 3 main columns
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-grid/wireframe-3columns.png)

### Creating 3 big columns
First **.col** will go inside first **.row**. Next **two columns** will go into the **second row**.

```html
<div class="container">
    <div class="row">
        <div class="col-12">
            <h1>.col</h1>
        </div>
    </div>
    <div class="row">
        <div class="col-4">
            <h1>.col-4</h1>
        </div>
        <div class="col-8">
            <h1>.col-8</h1>
        </div>
    </div>
</div>
```
#### Webpage with container, 2 main rows, 3 main columns, 1 row
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-grid/wireframe-1row.png)

### Creating row for small columns
Now we can nest row inside the **.col-8** column.

```html
<div class="container">
    <div class="row">
        <div class="col-12">
            <h1>.col</h1>
        </div>
    </div>
    <div class="row">
        <div class="col-4">
            <h1>.col-4</h1>
        </div>
        <div class="col-8">
            <div class="row">
                <h1>.row</h1>
            </div>
        </div>
    </div>
</div>
```
#### Webpage with container, 2 main rows, 3 main columns, 1 row, 4 small columns
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/new-grid/wireframe-4columns.png)

### Final step
Lets add four **.col-3** columns inside the row that we created in previous example.

```html
    <div class="container">
        <div class="row">
            <div class="col">
                <h1>.col</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-4">
                <h1>.col-4</h1>
            </div>
            <div class="col-8">
                <div class="row"
                    <div class="col-3">
                        <h1>.col-3</h1>
                    </div>
                    <div class="col-3">
                        <h1>.col-3</h1>
                    </div>
                    <div class="col-3">
                        <h1>.col-3</h1>
                    </div>
                    <div class="col-3">
                        <h1>.col-3</h1>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

## Responsive Grid
Is your website responsive? Is it mobile friendly?
Bootstrap Grid provides you with set of classes with specific **prefixes** that give you possibility to control how your layout would look on devices with different displays. The following table shows which class represents which display size.
![](https://github.com/toni-mo/bootstrap-grid/blob/master/img/responsiveness-table.PNG)

Lets use simple example code and try changing the width of the browser window which simulates different display size.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Responsive example</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" integrity="sha384-9gVQ4dYFwwWSjIDZnLEWnxCjeSWFphJiwGPXr1jddIhOegiu1FwO5qRGvFXOdJZ4" crossorigin="anonymous">
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col-lg-6 col-md-4 col-sm-3 col-12 border">
                <h1>.col-lg-6 .col-md-4 .col-sm-3 .col-12</h1>
            </div>
            <div class="col-lg-6 col-md-4 col-sm-3 col-12 border">
                <h1>.col-lg-6 .col-md-4 .col-sm-3 .col-12</h1>
            </div>
            <div class="col-lg-6 col-md-4 col-sm-3 col-12 border">
                <h1>.col-lg-6 .col-md-4 .col-sm-3 .col-12</h1>
            </div>
            <div class="col-lg-6 col-md-4 col-sm-3 col-12 border">
                <h1>.col-lg-6 .col-md-4 .col-sm-3 .col-12</h1>
            </div>
        </div>
    </div>
</body>
</html>
```

## Alignment
There are two types of alignment using Bootstrap Grid.
 1. Vertical alignment
 2. Horizontal alignment

You can achieve it by adding specific classes either to **row** or to **column**.

### Vertical alignment(for row)
Here we have to work with row and add following classes.
 * **.align-items-start** - aligns columns at the top of the row.
 * **.align-items-center** - aligns columns in the middle of the row.
 * **.align-items-end** - aligns columns at the bottom of the row.
 
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
Here we're working with column and adding following classes.
 * **.align-self-start** - aligns **only this** column at the top of the row.
 * **.align-self-center** - aligns **only this** column in the middle of the row.
 * **.align-self-end** - aligns **only this** column at the bottom of the row.
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
Working with row again and adding following classes.
 * **.justify-content-start** - aligns columns on the left, in the begining of the row.
 * **.justify-content-center** - aligns columns in the center of the row.
 * **.justify-content-end** - aligns columns on the right, in the end of the row.
 * **.justify-content-around** - aligns columns closer to the center with gap between and around the columns.
 * **.justify-content-between** - aligns columns at the left and right ends of the row with big gap between them.
 
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

## Offsetting
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
In all previous examples, for sake of simplicity, we didn't use any other elements than **<div>**. In reality we need to use proper semantic structure for our webpage. For example use class **.container** as child of such elements: `<header></header>`, `<main></main>`, `<footer></footer>`.
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

## Summary, Bootstrap Grid
 1. Easy to use, building grid system just with 3 main classes.
 2. Differen size columns.
 3. Responsive, mobile friendly.
 4. Alignment and offsetting.
 
## Useful Links
This guide displays only the most basic and essential features of the Bootstrap Grid. There are much more what can you do with it. Use official Bootstrap documentation and following links to get to know Bootrap Grid better!
 * [Bootstrap documentation](https://getbootstrap.com/)
 * [Bootstrap Grid](https://getbootstrap.com/docs/4.1/layout/grid/)
 * [W3School guide about Bootstrap Grid](https://www.w3schools.com/bootstrap4/bootstrap_grid_system.asp)
 
# Thank you!
