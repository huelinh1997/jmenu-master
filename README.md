# JMenu
A simple responsive CSS Menu library. JMenu requires no Javascript and it's 
easy to customize.

## Usage

### A Simple Menu

1. Add the JMenu stylesheet to the header of your site:
```html
<link rel="stylesheet" href="css/jmenu.min.css">
```

2. Add the basic markup for your menu:

```html
<nav class="jmenu">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Categories</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

### Dropdowns
1. To add a dropdown add the `.jm-dropdown` class to the menu item:
```html
<nav class="jmenu">
  <ul>
    <li><a href="#">Home</a></li>
    <li class="jm-dropdown"><a href="#">Categories</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

2. Nest the dropdown list inside of the `li` element after the anchor:
```html
<nav class="jmenu">
  <ul>
    <li><a href="#">Home</a></li>
    <li class="jm-dropdown">
      <a href="#">Categories</a>
      <ul>
        <li><a href="#">Apples</a></li>
        <li><a href="#">Bananas and Pears</a></li>
        <li><a href="#">Oranges</a></li>
      </ul>
    </li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

3. (Optional) Add a caret to the dropdown with a span styled 
`jm-icon-dropdown`:
```html
<nav class="jmenu">
  <ul>
    <li><a href="#">Home</a></li>
    <li class="jm-dropdown">
      <a href="#">Categories <span class="jm-icon-dropdown"></span></a>
      <ul>
        <li><a href="#">Apples</a></li>
        <li><a href="#">Bananas and Pears</a></li>
        <li><a href="#">Oranges</a></li>
      </ul>
    </li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

### Menu Button 
1. To create a menu button add a checkbox and label before the first menu 
list. Make sure they have the class `.jm-menu-btn`:
```html
<nav class="jmenu">
  <label for="menu-btn" class="jm-menu-btn">Menu</label>
  <input type="checkbox" id="menu-btn" class="jm-menu-btn">
  <ul>
    <li><a href="#">Home</a></li>
    <li class="jm-dropdown">
      <a href="#">Categories</a>
      <ul>
        <li><a href="#">Apples</a></li>
        <li><a href="#">Bananas and Pears</a></li>
        <li><a href="#">Oranges</a></li>
      </ul>
    </li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

2. Add the `.jm-collapse` class to the menu list:
```html
<nav class="jmenu">
  <label for="menu-btn" class="jm-menu-btn">Menu</label>
  <input type="checkbox" id="menu-btn" class="jm-menu-btn">
  <ul class="jm-collapse">
    <li><a href="#">Home</a></li>
    <li class="jm-dropdown">
      <a href="#">Categories</a>
      <ul>
        <li><a href="#">Apples</a></li>
        <li><a href="#">Bananas and Pears</a></li>
        <li><a href="#">Oranges</a></li>
      </ul>
    </li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

3. (Optional) To add a hamburger icon, add the `jm-icon-menu` class to the 
button label:
```html
<nav class="jmenu">
  <label for="menu-btn" class="jm-menu-btn jm-icon-menu">Menu</label>
  <input type="checkbox" id="menu-btn" class="jm-menu-btn">
  <ul class="jm-collapse">
    <li><a href="#">Home</a></li>
    <li class="jm-dropdown">
      <a href="#">Categories</a>
      <ul>
        <li><a href="#">Apples</a></li>
        <li><a href="#">Bananas and Pears</a></li>
        <li><a href="#">Oranges</a></li>
      </ul>
    </li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

## Customization

### Typography

JMenu is designed to pick up typographic styles from your website's
stylesheet. By default the menu items will inherit their parent container's 
style. You can change that by overriding the `.jmenu` class.

```css
.jmenu {
  font: bold 1.125em 'Helvetica', sans-serif;
}
```

To change the color of the menu item links, simply override `.jmenu a` with 
new colors.

```css
.jmenu a {
  color: coral;
}

.jmenu a:hover {
  color: red;
}
```

To change the colors of dropdown links it's a little more involved. Make sure
you override both selectors for the dropdown links or they won't display 
properly.
```css
.jm-dropdown ul a,
.jm-dropdown:hover ul a {
  color: #0072bc; /* Blue */
}

.jm-dropdown ul a:hover,
.jm-dropdown:hover ul a:hover {
  color: #000; /* Black*/
}
```

### Menu Bar

To change the look of the menu bar override the background style of the
`.jmenu` class.
```css 
.jmenu {
  background: #ccc; /* Changes menu bar to a light gray */
}
```

### Dropdowns

Override the `.jm-dropown ul` class to change the styling of the dropdowns.


## Compatibility

JMenu has been tested in the following browsers:
* Chrome 67 (Mobile and Desktop
* Firefox 60
* Safari 11 (Mobile and Desktop)
* Internet Explorer 10
* Edge 42 

