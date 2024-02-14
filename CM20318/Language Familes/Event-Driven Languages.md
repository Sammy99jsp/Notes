*Purpose*: Interactive systems
*Examples*: Visual Basic, JavaScript, GTK & Qt through C(++).

This can be though of as an approach to programming rather than a family of languages.

Event-driven languages are used extensively for UI, interactive applications, and even simulations (languages like Simula, SPICE, etc.).

## Event Loops
Usually event-driven code has a big 'main' loop which cycles forever, and corresponding event handlers are called:
```rust
loop {
  let event = get_next_event();
  match event {
	Event::Click(client_ev) => click_handler(click_ev),
	Event::KeyPress(keypress_ev) => key_handler(keypress_ev),
	_ => {}
  }
}
```
