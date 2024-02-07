UIs can be thought of being a combination of three things:
1. Rendering the UI (Output)
2. [Event Handlers|Event handling] (Input)
3. State management.

### Example — A Button
![[Pasted image 20240207115901.png]]
We can model UI widgets as state machines: here, the button has two states which transition between each other based on input events.

All widgets are implemented in a similar state-based way due to their nature, where states are the outputs, and input events cause transitions between these states.