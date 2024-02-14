Related to [[Object-Oriented Languages]].

*Purpose*: general programming, simulation, concurrent systems
*Languages*: Pony, Erlang, Elixir
*Features*: using messaging.

An *actor* is an entity or object that communicate with other actors through messages.

When an actor receives a message, it can:
- do some computation and modify its internal state
- send messages to other actors
- create new actors

The message-passing is more easy to parallelise as no one actor shares state with an other.

Actor languages often rely on efficient runtimes to schedule when actors actually act.