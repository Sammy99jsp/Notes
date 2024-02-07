The Model-View-Controller (MVC) pattern is omnipresent for implementing such state machines. They consist of:
- The **model**, storing the *state* of the data the UI is presenting.
- The **view**, which visualises the data (rendering).
- The **controller**, which does the hard work of:
	- managing the state machine in response to input events,
	- executing commands, and 
	- updating the model.
