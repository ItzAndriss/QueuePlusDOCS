# Lobby balancer

QueuePlus automatically routes players to the best lobby available.

***

## Configuration

```toml
[servers.lobbies]
list = ["lobby1", "lobby2", "lobby3"]
```

When a player uses `/lobby` or `/hub`, QueuePlus:

{% stepper %}
{% step %}
### Ping lobbies

Pings each lobby to check availability and responsiveness.
{% endstep %}

{% step %}
### Determine counts

Gathers current player counts from each lobby.
{% endstep %}

{% step %}
### Connect player

Connects the player to the least populated lobby.
{% endstep %}
{% endstepper %}

***

## Example

If:

* lobby1 = 40/100 players
* lobby2 = 12/100 players
* lobby3 = 25/100 players

Then `/lobby` will send the player to **lobby2** automatically.
