# Parancsok

A QueuePlus játékos és admin parancsokat is tartalmaz.

***

## Játékos parancsok

| Parancs              | Leírás                                      |
| -------------------- | ------------------------------------------- |
| `/queue <szerver>`   | Hozzáad a megadott szerver várólistájához  |
| `/leavequeue`        | Eltávolít a jelenlegi várólistádról         |
| `/lobby` vagy `/hub` | A legkevésbé telített lobby szerverre küld  |

**Példa:**

{% code title="Játékos példa" %}
```bash
/queue survival

# -> A survival szerver várólistájára kerültél (Pozíciód: 3/15)
```
{% endcode %}

***

## Admin parancsok

| Parancs                       | Leírás                                             |
| ----------------------------- | -------------------------------------------------- |
| `/queuestart <szerver>`       | Engedélyezi a várólistát az adott szerveren       |
| `/queuestop <szerver>`        | Letiltja a várólistát az adott szerveren          |
| `/queuedev <szerver> on/off`  | Fejlesztői mód ki- vagy bekapcsolása egy szerveren |
| `/queuereload`                | Újratölti a konfigurációt és a fejlesztői mód állapotát |

**Példa:**

{% code title="Admin példa" %}
```bash
/queuedev skyblock on

# -> A skyblock szerver fejlesztői módja most ENGEDÉLYEZVE.
```
{% endcode %}
