## HTML Lists
HTML lists allow web developers to group a set of related items in lists.

### Example
An unordered HTML list:
- Item
- Item
- Item
- Item

An ordered HTML list:

1. First Item
2. second Item
3. third Item
4. Fourth Item

## Unordered HTML List
An unordered list starts with the <ul> tag. Each list item starts with the <li> tag.
The list items will be marked with bullets (small black circles) by default:
  ### Example 
  <ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
  
## Ordered HTML List
An ordered list starts with the <ol> tag. Each list item starts with the <li> tag.
The list items will be marked with numbers by default:
  ### Example
  <ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
  ## HTML Description Lists
HTML also supports description lists.
A description list is a list of terms, with a description of each term.
The <dl> tag defines the description list, the <dt> tag defines the term (name), and the <dd> tag describes each term:
  ### Example 
  <dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
  ## HTML List Tags
Tag	  Description
<ul>	Defines an unordered list
<ol>	Defines an ordered list
<li>	Defines a list item
<dl>	Defines a description list
<dt>	Defines a term in a description list
<dd>	Describes the term in a description list
  .....................................................................................................................
  ## Control flow with JS
The control flow is the order in which the computer executes statements in a script.
Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops. 
For example, imagine a script used to validate user data from a webpage form. The script submits validated data, but if the user, say, leaves a required field empty, the script prompts them to fill it in. To do this, the script uses a conditional structure or if...else, so that different code executes depending on whether the form is complete or not:
 
  if (field==empty) {
    promptUser();
} else {
    submitForm();
  .....................................................................................................................
  ## The CSS Box Model
In CSS, the term "box model" is used when talking about design and layout.
The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content. The image below illustrates the box model:
 
  ### Explanation of the different parts:
  Content - The content of the box, where text and images appear
. Padding - Clears an area around the content. The padding is transparent
. Border - A border that goes around the padding and content
. Margin - Clears an area outside the border. The margin is transparent
   The box model allows us to add a border around elements, and to define space between elements. 
  
  Example
Demonstration of the box model:

div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}


  
  
