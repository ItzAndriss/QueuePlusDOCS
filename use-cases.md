# Használati esetek

Így viselkedik a QueuePlus valós szerverhelyzetekben.

***

## Szerver újraindítás példa

{% stepper %}
{% step %}
### A szerver újraindul

A `Kingdoms` szerver újraindul.
{% endstep %}

{% step %}
### Kapcsolat bontásának észlelése

A QueuePlus a `KickedFromServerEvent` eseményen keresztül érzékeli a kapcsolat megszakadását.
{% endstep %}

{% step %}
### Játékosok visszahelyezése a várólistára

A játékosok automatikusan visszakerülnek a `Kingdoms` várólistájára.
{% endstep %}

{% step %}
### Visszaszámlálás megjelenítése

A visszaszámlálás megjelenik az ActionBar felületén.
{% endstep %}

{% step %}
### Újracsatlakozás a várakozási idő után

A `wait-after-restart` másodperc letelte után a játékosok automatikusan visszacsatlakoznak.
{% endstep %}
{% endstepper %}

***

{% hint style="info" %}
### Fejlesztői tesztelés

* Engedélyezd ezzel: `/queuedev skyblock on` karbantartás előtt.
* Teszteld a szerver funkcióit anélkül, hogy más játékosok csatlakozhatnának.
* Később kapcsold ki ezzel: `/queuedev skyblock off`.
{% endhint %}

{% hint style="info" %}
### Több-lobbis hálózatok

* Használd a `[servers.lobbies]` beállítást a terhelés elosztásához.
* A `/lobby` parancs segítségével az új játékosok egyenletesen oszlanak el a lobbyk között.
{% endhint %}
