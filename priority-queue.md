# Priority queue

QueuePlus can integrate with LuckPerms to give specific ranks faster queue access.

## How It Works

Each player’s priority is determined by their highest matching permission:

```
queue.priority.<n>
```

Where `<n>` is an integer from **1 to 10** (1 = lowest, 10 = highest).

When multiple players are queued:

* Higher priority players are placed ahead of lower priority ones.
* Players with the same priority keep their position order (FIFO).

## Example

| Player |          Permission | Position |
| ------ | ------------------: | -------: |
| Admin  | `queue.priority.10` |        1 |
| Alex   |  `queue.priority.5` |        2 |
| Steve  |  `queue.priority.1` |        3 |

After re-sorting by priority, Admin goes first, then Alex, then Steve.

{% hint style="info" %}
If no permission system (like LuckPerms) is detected, QueuePlus defaults to FIFO (first-come, first-served).
{% endhint %}
