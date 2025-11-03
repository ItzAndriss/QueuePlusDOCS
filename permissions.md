# Jogosultságok

| Jogosultság           | Leírás                                               |
| --------------------- | ---------------------------------------------------- |
| `queue.use`           | Engedélyezi a `/queue` parancs használatát           |
| `queue.leave`         | Engedélyezi a `/leavequeue` parancs használatát      |
| `queue.admin`         | Hozzáférést ad az admin parancsokhoz                 |
| `queue.dev.<server>`  | Engedélyezi a csatlakozást egy adott szerverhez fejlesztői módban |
| `queue.priority.<n>`  | Várólista prioritási szint (1–10)                    |

{% hint style="info" %}
A magasabb szám magasabb prioritást jelent. Az azonos szintű játékosokat a csatlakozási sorrend (FIFO) alapján rendezi a rendszer.
{% endhint %}

***

## Prioritás beállítási példa (LuckPerms)

{% code title="LuckPerms: csoport prioritások beállítása" %}
```bash
/lp group default permission set queue.priority.1 true
/lp group vip permission set queue.priority.5 true
/lp group admin permission set queue.priority.10 true
```
{% endcode %}

***

## Fejlesztői mód példa

Ha egy szerver fejlesztői módban van, csak a megfelelő fejlesztői jogosultsággal rendelkező játékosok csatlakozhatnak.

{% code title="LuckPerms: felhasználói fejlesztői jogosultság beállítása" %}
```bash
/lp user Andris permission set queue.dev.survival true
```
{% endcode %}
