# Use cases

Here’s how QueuePlus behaves in real server situations.

***

## Server Restart Example

{% stepper %}
{% step %}
### Server restarts

`Kingdoms` server restarts.
{% endstep %}

{% step %}
### Disconnection detected

QueuePlus detects disconnections via `KickedFromServerEvent`.
{% endstep %}

{% step %}
### Players requeued

Players are automatically requeued for `Kingdoms`.
{% endstep %}

{% step %}
### Countdown shown

Countdown appears in their ActionBar.
{% endstep %}

{% step %}
### Reconnect after wait

After `wait-after-restart` seconds, players reconnect.
{% endstep %}
{% endstepper %}

***

{% hint style="info" %}
### Developer Testing

* Enable with: `/queuedev skyblock on` before maintenance.
* Test server features without public players joining.
* Disable later with: `/queuedev skyblock off`.
{% endhint %}

{% hint style="info" %}
### Multi-Lobby Networks

* Use `[servers.lobbies]` to balance load.
* Use `/lobby` to ensure new joins are distributed evenly.
{% endhint %}
