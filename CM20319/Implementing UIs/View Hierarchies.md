## What is a view hierarchy?
View hierarchies compose multiple widgets into a UI by utilising a tree structure.

Each widget can contain 0+ child widgets. This leads to a tree structure (view trees) ending at the root node, which has no children.

The JSX source code here shows an example of this tree-like structure:
```jsx
<Grid>
  <Row>
    <Column>1</Column>
    <Column>2</Column>
    <Column>3</Column>
  </Row>
  <Row>
	<Column>4</Column>
	<Column>5</Column>
	<Column>6</Column>
  </Row>
  <Row>
	<Column>7</Column>
	<Column>8</Column>
	<Column>9</Column>
  </Row>
</Grid>
```

Here, `<Grid></Grid>` is the root widget.
## How are they used?
View hierarchies can:
- Change their output by mutating the view tree.
	- Redraw only the parts of the UI that change.
- Input-wise:
	- propagate input events upwards,
	- have custom events, and
	- contain their own event handlers.
- Automatically position and size views by traversing the tree.
