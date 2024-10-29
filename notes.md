
# HTML YAP

## Head - Metadata, External Links, Title
- **Meta Data**: Info about info
  - `meta name="description"` (brief summary of the page's content)
  - `meta name="keywords"` (words used to influence SEO)
  - `meta name="robots"` (indexing and following links)
- **Emmet Abbreviations**: 
  - Basic structure, `lorem ipsum`, `p*n` instead of pasting `<p></p>` n times

## Body - Headers and Paragraphs
- **Text Formatting**:
  - `strong` = bold `<b>`
  - `emphasised` = italicised `<i>`
- **Self-Closing Tags**: 
  - `<br>`, `<hr>` (horizontal rule)
- **Anchor Tag**: 
  - `<a href="link">text</a>` and to open the link in a new page: `<a href="link" target="_blank">text</a>`
- **Attributes**: Give properties or characteristics to a tag
- **Image Tag**: 
  - `<img src="" alt="" width="" height="">` (alt is the text visible when the image doesn't load or is inaccessible)

## Lists and Tables
- **Lists**: 
  - `<ul type="">`, `<ol>`
- **Table Structure**:
  ```html
  <table>
      <thead>
          <tr>
              <th></th> <!-- Table header -->
          </tr>
      </thead>
      <tbody>
          <tr>
              <td></td> <!-- Table data -->
          </tr>
      </tbody>
  </table>
  ```

## Forms - Used to Collect User Input
- **Input Types**: 
  - `<input type="text/radio/checkbox/submit/button/reset" placeholder="">`
- **Textarea**: 
  - `<textarea name="" rows="" cols=""></textarea>` (for bigger user inputs)

### Form Example
```html
<form action="backend.php">
    <label for="fname">First Name:</label>
    <input type="text" id="fname" name="fname">
</form>
```
- **Shortcuts**: `input:type` automatically gives you all the required elements
- **Shortcut**: `Alt + Arrow Key` to move a block of selected text around

- **Div Tag**: Brings about a division; it is a block element
- **Dropdown**: 
  ```html
  <select name="" id="">
      <option value="name">Text</option>
  </select>
  ```
  Adding `"selected"` next to `value=""` causes that particular option to be selected by default

## Inline and Block Elements
- **Block Element**: Takes up the entire width
- **Inline Element**: Only uses as much space as required
  - `<span>` is an inline element
- **Emmet Shortcuts**: 
  - `span.classname`, `span#id`
  - General shortcut: `div.class1.class2.class3` for multiple classes

## IDs and Classes
- **ID**: Unique
- **Classes**: Can be reused

## HTML Entities
- `&nbsp` - Non-breaking space
- `<p>` has to be written as `&lt;p&gt;`
- `&copy;` for copyright symbol 
- Empty character - `&#8203;`

## Semantic Tags
- `<header>`, `<nav>`, `<section>`, `<footer>`, etc.
- `<figure>`, `<main>`, `<summary>`, `<details>`, `<summary>text</summary>` (hidden answer)

## MDN
- Mozilla Development Network (useful for HTML resources)

---

# CSS - Cascading Style Sheets + JS

## Basic Syntax
- `selector { property: value; }`
- `* { /* universal selector */ }`

## Internal CSS
- Within `<head>` tag
- `<link rel="stylesheet" href="name.css">`
- Shortcut to add stylesheet: `link:css`
- Using `!important` to make an inline CSS have higher precedence over an external CSS

## Selectors
- `#name { style }` where `name` is the `id=""`
- `.name { style }` where `name` is the `class=""`
- `x, y { style }` for a group of selectors

## Background Color Shortcut
- `bcol`

## User Agent Stylesheet
- In Google Developer Tools

## Fonts
- **Web Safe Fonts**: Preinstalled with the OS 
- **Font Stack**: List of fonts specified in the `font-family`, in order of preference
- **Web Fonts**: Fonts that have to be imported
  ```html
  <link href="">
  ```
- **Line Height**: Distance between characters above the selected text (em is a unit)

## Border Properties
- `border: color style width;` can be written in 1 line
- **Background Image**: `background-image: url(image);` with `repeat-x`, `repeat-y`, and `no-repeat`

## Box Model
- **Components**: Padding, Margin, Border
- **Padding/Margin**: Top, Right, Bottom, Left (replace with actual pixel values)
- **Border Sizing**: Refers to how the browser calculates the width and height of an element
  - `border-sizing: content-box (default) / border-box / initial / inherit`

## Margin
- `margin: auto;` for centering

## Float and Clear
- `float: left;` (specifies whether an element should float)
- `clear: right/left;` (no overlapping)
- `clear: both;` (avoids interference)

## Button Properties
- `cursor: pointer;`
- To remove the underline from a hyperlink: `text-decoration: none;`

## Pseudo-Classes
- `name:hover { properties }` (for changes on hover)
- `name:visited {}` 
- `name:active {}`

## Navigation Menu
- Comes under `<header>` tag
- `navbar`, `navbar ul`, `navbar li`
- `.navbar ul { overflow: auto; }`

## Inline-Block
- Allows an element to be displayed horizontally alongside others (like inline) while also enabling width and height settings

## Positioning
- **Static**: Default
- **Absolute**: Relative to the parent
- **Relative**: Relative to its normal position
- **Fixed**: Doesn't move when scrolled
- **Sticky**: Sticks to the top of the browser

## Visibility and Z-Index
- **Visibility**: visible (default), hidden
- **Display**: `display: none;` (removes the element without reserving space)
- **Z-Index**: Works only for non-default static positioned elements; controls the order of overlap (higher z-index on top)

## Flexbox
- `display: flex;` (parent) and all children become flex items
- Shortcut for printing numbered text boxes: `div.item#item-$*6` (creates 6 divs with class item each with id {item-n} from 1 to 6)
- `flex-direction: ...`
- `flex-wrap: wrap;` (elements will move to the next line)
- **Justify Content**: `space-between`, `space-evenly`, `space-out`

## Flex Properties
- **Order**: Controls visual order of flex items
- **Flex Grow**: Distributes excess space among flex items
- **Flex Basis**
- **Flex Shrink**

## Responsive Design
- Font size relative to root element using `em` & `rem`
- `vh` - view height, `vw` - view width (100vh for full height)

## JavaScript Events
- Using `event` and `event.currentTarget`
  ```javascript
  const heading = document.querySelector("h1");
  heading.addEventListener("click", function(event) {
      event.currentTarget.classList.add("class");
  });
  ```
- `console.log(event.type)` -> will return "click"
- `event.preventDefault()` prevents default behavior (useful with forms)

## Applying to Multiple Instances
- Example with buttons:
  ```javascript
  const btns = document.querySelectorAll('.btn');
  btns.forEach(function(btn) {
      btn.addEventListener('click', function(e) {
          e.currentTarget.style.color = "green";
      });
  });
  ```

## Event Propagation
- **Event Bubbling**
- **Event Capturing**

## Media Queries

## Form Submissions
- Accessing values: `name.value`, etc.

## Local Storage vs Session Storage
- **Local Storage**: Stays even after the browser closes
- **Session Storage**: Gets wiped
- **Methods**:
  - `localStorage.setItem('key', 'value');`
  - `sessionStorage.setItem('name', 'john');`
  - `localStorage.getItem('key');` will return the related value
  - `localStorage.removeItem('key');`
  - `localStorage.clear();` // no keys nor values left

## JSON Methods
- `JSON.stringify()`: Converts a JS value into a JSON string 
- `JSON.parse()`

### Example:
```javascript
const friends = ['john', 'peter', 'bob'];
localStorage.setItem('friends', JSON.stringify(friends));
// Now stored as an array
const values = JSON.parse(localStorage.getItem('friends'));
// Access elements using index
console.log(values[2]);


```
```