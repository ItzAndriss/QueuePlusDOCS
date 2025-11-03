# Lobby terheléselosztó

A QueuePlus automatikusan a legmegfelelőbb lobby szerverre irányítja a játékosokat.

***

## Konfiguráció

```toml
[servers.lobbies]
list = ["lobby1", "lobby2", "lobby3"]
```

Amikor egy játékos a `/lobby` vagy `/hub` parancsot használja, a QueuePlus a következő lépéseket hajtja végre:

{% stepper %}
{% step %}
### Lobby-k pingelése

Lepingi az összes lobbyt, hogy ellenőrizze azok elérhetőségét és válaszképességét.
{% endstep %}

{% step %}
### Játékosszámok meghatározása

Összegyűjti az aktuális játékosszámokat minden lobbyból.
{% endstep %}

{% step %}
### Játékos csatlakoztatása

A játékost a legkevésbé telített lobby szerverre csatlakoztatja.
{% endstep %}
{% endstepper %}

***

## Példa

Ha:

* lobby1 = 40/100 játékos
* lobby2 = 12/100 játékos
* lobby3 = 25/100 játékos

Akkor a `/lobby` parancs automatikusan a **lobby2** szerverre küldi a játékost.
