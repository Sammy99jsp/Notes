The Model-View-Controller (MVC) pattern is omnipresent for implementing such state machines. They consist of:
- The **model**, storing the *state* of the data the UI is presenting.
- The **view**, which visualises the data (rendering).
- The **controller**, which does the hard work of:
	- managing the state machine in response to input events,
	- executing commands, and 
	- updating the model.

An example MVC pattern for the previous button example is in this code:
```tsx
// Model
let mouse_over = false;
let is_pressed = false;

// View
if (is_pressed) {
  display(<PressedButton></PressedButton>);
} else {
  display(<UnpressedButton></UnpressedButton>);
}

// Controller
Mouse.onMove((position) => mouse_over = self.is_inside(position));
Mouse.onButton((pressed) => is_pressed = mouse_over && pressed);
```