# Prioritásos várólista

A QueuePlus integrálható a LuckPerms bővítménnyel, hogy bizonyos rangok gyorsabban jussanak sorra a várólistán.

## Működési elv

Minden játékos prioritása a legmagasabb érvényes jogosultsága alapján kerül meghatározásra:

```
queue.priority.<n>
```

Ahol `<n>` egy **1 és 10** közötti egész szám (1 = legalacsonyabb, 10 = legmagasabb).

Ha több játékos van a várólistán:

* A magasabb prioritású játékosok előrébb kerülnek.
* Az azonos prioritású játékosok a csatlakozási sorrend (FIFO) alapján maradnak rendezve.

## Példa

| Játékos |          Jogosultság | Pozíció |
| ------- | -------------------: | -------: |
| Admin   | `queue.priority.10`  |        1 |
| Alex    |  `queue.priority.5`  |        2 |
| Steve   |  `queue.priority.1`  |        3 |

A prioritás szerinti újrarendezés után az Admin kerül előre, majd Alex, végül Steve.

{% hint style="info" %}
Ha nem található engedélykezelő rendszer (például LuckPerms), a QueuePlus alapértelmezetten a FIFO elvet alkalmazza (érkezési sorrend alapján).
{% endhint %}
