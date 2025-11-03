# Konfiguráció

A QueuePlus minden beállítást a `plugins/Queue/config.toml` fájlban tárol.\
Ez a fájl **TOML** formátumot használ — hasonló a YAML-hoz, de egyszerűbb.

***

## Példa konfiguráció

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

# több lobby a /lobby parancshoz
[servers.lobbies]
list = ["lobby1", "lobby2", "lobby3"]

[queue.priority]
enabled = true
max-level = 5
permission-prefix = "queue.priority."

[messages]
# -- Alap várólista üzenetek --
queued = "§eVárólistára kerültél a §b{server}§e szerverre... (Pozíció: §a{position}§e/{total})"
queued-actionbar = "§eVárakozás a §b{server}§e szerverre... §7({position}/{total})"
joining = "§aCsatlakozás a {server} szerverhez..."
requeued = "§eA {server} újraindul, visszakerültél a várólistára."
joining-lobby = "§aCsatlakozás a §b{server}§a lobbyhoz..."

# -- Hiba / figyelmeztető üzenetek --
server-down = "§cA szerver jelenleg nem elérhető, kérlek várj..."
server-starting = "§eA szerver indul... §7({remaining}s)"
unknown-server = "§cIsmeretlen szerver: {server}"
same-server = "§eMár a {server} szerveren vagy."
queue-disabled = "§cA várólista ideiglenesen le van tiltva ezen: {server}!"
queue-enabled = "§aA várólista engedélyezve lett ezen: {server}!"
no-lobby = "§cJelenleg nincs elérhető lobby szerver!"

# -- Várólista parancs üzenetek --
queue-usage = "§eHasználat: /queue <server> | §7Elérhető szerverek: {servers}"
queue-reload = "§aA várólista konfiguráció újratöltve!"
unknown-command-server = "§cIsmeretlen szerver: {server}"
toggle-usage = "§eHasználat: /{command} <server>"

# -- Fejlesztői mód (dev mode) --
dev-usage = "§eHasználat: /queuedev <server> <on/off>"
dev-mode = "§eFejlesztői mód a {server} szerveren: {status}"
dev-status-on = "§aENGEDÉLYEZVE"
dev-status-off = "§cLETILTVA"
dev-active = "§cA {server} fejlesztői módban van, nem csatlakozhatsz!"
dev-permission = "§cCsak fejlesztők csatlakozhatnak a {server} szerverhez."

# -- /leavequeue parancs --
queue-left = "§aKiléptél a várólistáról!"
queue-not-in = "§eNem vagy egyetlen várólistán sem."

# -- Egyéb --
server-unavailable = "§cA {server} jelenleg nem elérhető."
```
{% endcode %}

***

## Fontos kulcsok

| Kulcs                | Leírás                                                                     |
| -------------------- | --------------------------------------------------------------------------- |
| `max-players`        | A szerver által támogatott maximális játékosszám                           |
| `wait-after-restart` | Mennyi ideig kell várni (másodpercben) újracsatlakozás előtt újraindítás után |
| `dev-permission`     | Az engedély, amely szükséges a fejlesztői mód alatti csatlakozáshoz          |

***

## Helyettesítők (placeholderek)

| Helyettesítő | Leírás                                      |
| ------------- | ------------------------------------------- |
| `{server}`    | Célzott szerver neve                        |
| `{position}`  | Játékos pozíciója a várólistán              |
| `{total}`     | Összes várakozó játékos                     |
| `{remaining}` | Hátralévő másodpercek az elérhetőségig      |
| `{status}`    | Fejlesztői mód állapota (ENGEDÉLYEZVE/LETILTVA) |
