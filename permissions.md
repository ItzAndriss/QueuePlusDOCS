# Permissions

| Permission           | Description                                      |
| -------------------- | ------------------------------------------------ |
| `queue.use`          | Allows using `/queue`                            |
| `queue.leave`        | Allows `/leavequeue`                             |
| `queue.admin`        | Grants access to admin commands                  |
| `queue.dev.<server>` | Allows joining a specific server during dev mode |
| `queue.priority.<n>` | Priority queue level (1–10)                      |

{% hint style="info" %}
Higher numbers = higher priority. Players with the same level are sorted by join order (FIFO).
{% endhint %}

***

## Priority Setup Example (LuckPerms)

{% code title="LuckPerms: set group priorities" %}
```bash
/lp group default permission set queue.priority.1 true
/lp group vip permission set queue.priority.5 true
/lp group admin permission set queue.priority.10 true
```
{% endcode %}

***

## Developer Mode Example

If a server is in developer mode, only players with the matching dev permission can join.

{% code title="LuckPerms: set user dev permission" %}
```bash
/lp user Andris permission set queue.dev.survival true
```
{% endcode %}
