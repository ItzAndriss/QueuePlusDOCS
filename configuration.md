# Configuration

QueuePlus stores all settings in `plugins/Queue/config.toml`.\
This file uses the TOML format — similar to YAML but simpler.

***

## Example Configuration

{% code title="plugins/Queue/config.toml" %}
```toml
check-interval = 1

[servers]

[servers.survival]
max-players = 80
wait-after-restart = 25
dev-permission = "queue.dev.survival"

[servers.skyblock]
max-players = 60
wait-after-restart = 20
dev-permission = "queue.dev.skyblock"

[servers.mines]
max-players = 70
wait-after-restart = 30
dev-permission = "queue.dev.mines"

# multiple lobbies for /lobby command
[servers.lobbies]
list = ["lobby1", "lobby2", "lobby3"]

[queue.priority]
enabled = true
max-level = 5
permission-prefix = "queue.priority."

[messages]
# -- Base queue messages --
queued = "§eYou are queued for §b{server}§e... (Position: §a{position}§e/{total})"
queued-actionbar = "§eWaiting for §b{server}§e... §7({position}/{total})"
joining = "§aConnecting to {server}..."
requeued = "§e{server} is restarting, you have been added back to the queue."
joining-lobby = "§aConnecting to §b{server}§a lobby..."

# -- Error / warning messages --
server-down = "§cThe server is currently unavailable, please wait..."
server-starting = "§eThe server is starting up... §7({remaining}s)"
unknown-server = "§cUnknown server: {server}"
same-server = "§eYou are already on {server}."
queue-disabled = "§cThe queue is temporarily disabled for {server}!"
queue-enabled = "§aQueue enabled for {server}!"
no-lobby = "§cNo available lobby servers right now!"

# -- Queue command messages --
queue-usage = "§eUsage: /queue <server> | §7Available servers: {servers}"
queue-reload = "§aQueue configuration reloaded!"
unknown-command-server = "§cUnknown server: {server}"
toggle-usage = "§eUsage: /{command} <server>"

# -- Developer mode (dev mode) --
dev-usage = "§eUsage: /queuedev <server> <on/off>"
dev-mode = "§eDeveloper mode for {server}: {status}"
dev-status-on = "§aENABLED"
dev-status-off = "§cDISABLED"
dev-active = "§c{server} is in developer mode, you cannot join!"
dev-permission = "§cOnly developers can join {server}."

# -- /leavequeue command --
queue-left = "§aYou have left the queue!"
queue-not-in = "§eYou are not in any queue."

# -- Other --
server-unavailable = "§c{server} is currently unavailable."
```
{% endcode %}

***

## Important Keys

| Key                  | Description                                                              |
| -------------------- | ------------------------------------------------------------------------ |
| `max-players`        | The maximum number of players the backend server supports                |
| `wait-after-restart` | How long to wait (in seconds) before players can reconnect after restart |
| `dev-permission`     | Permission required to join a server while in developer mode             |

***

## Placeholders

| Placeholder   | Description                        |
| ------------- | ---------------------------------- |
| `{server}`    | Target server name                 |
| `{position}`  | Player's position in queue         |
| `{total}`     | Total queued players               |
| `{remaining}` | Remaining seconds before available |
| `{status}`    | Developer mode status (ON/OFF)     |
