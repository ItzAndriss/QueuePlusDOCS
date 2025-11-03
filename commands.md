# Commands

QueuePlus includes both player and admin commands.

***

## Player Commands

| Command            | Description                            |
| ------------------ | -------------------------------------- |
| `/queue <server>`  | Adds you to a server queue             |
| `/leavequeue`      | Removes you from your current queue    |
| `/lobby` or `/hub` | Sends you to the least populated lobby |

**Example:**

{% code title="Player example" %}
```bash
/queue survival

# -> You are queued for survival (Position: 3/15)
```
{% endcode %}

***

## Admin Commands

| Command                     | Description                                   |
| --------------------------- | --------------------------------------------- |
| `/queuestart <server>`      | Enables the queue for a specific server       |
| `/queuestop <server>`       | Disables queueing for that server             |
| `/queuedev <server> on/off` | Toggles developer mode for a specific server  |
| `/queuereload`              | Reloads the configuration and dev mode states |

**Example:**

{% code title="Admin example" %}
```bash
/queuedev skyblock on

# -> Developer mode for skyblock is now ENABLED.
```
{% endcode %}
