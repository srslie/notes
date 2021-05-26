
Block A block-level element occupies the entire width of its parent element (container), thereby creating a “block.”
Inline An inline-level element only occupies the space bounded by the tags defining the element, instead of breaking the flow of the content.
  <a> is used to create links
  <em> is used to denote that you’d like to emphasize some text.
  <strong> is used to denote that this text is important.

Inline-block An inline-block level element behaves the same as an inline element, but you can set a fixed width and/or height (note: no elements are inline-block by default)
<div> is a block element.
<span> is an inline element.

If you want to center an element, you can give the margin property a value of 0 auto to center a block-like element!

The display property allows us to change the default value of block and inline level elements.
display: inline-block;
display: inline;
display: block;
display: none;

hiding things:
// Element no longer exists on the page and does not take up space
display: none;

// Element exists on the page and takes up space but cannot be seen
visability: hidden

// Similar to visability, but is read by screen readers. Also useful for animation!
opacity: 0

flexbox - a layout method for laying out items in rows or columns. Items flex to fill additional space and shrink to fit into smaller spaces
display - a css property that sets whether an element is treated as a block or inline element and the layout used for its children, such as grid or flex
flex parent or flex container - Any HTML element that has been given the display: flex declaration
flex child or flex item - Any immediate descendants of a flex parent
main axis – the primary axis along which flex items are laid out. It can be horizontal or vertical, and is defined by the direction set by the flex-direction property.
On this Page
Syntax
Examples
Specifications
Browser compatibility
See also
The :nth-child() CSS pseudo-class matches elements based on their position in a group of siblings.
