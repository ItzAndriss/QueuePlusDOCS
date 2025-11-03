# Telepítés

## Követelmények

* Velocity 3.2 vagy újabb verzió
* Java 17 vagy újabb verzió
* Opcionális: LuckPerms a várólista-prioritás integrációhoz

## Telepítési lépések

{% stepper %}
{% step %}
### A plugin letöltése

Töltsd le a legújabb `QueuePlus.jar` fájlt.
{% endstep %}

{% step %}
### A plugin telepítése

Helyezd el a fájlt a Velocity `plugins/` könyvtárába.
{% endstep %}

{% step %}
### Indítsd el egyszer a proxy-t

Indítsd el egyszer a proxy-t — ez létrehozza a konfigurációs mappát:

```
/plugins/Queue/
├─ config.toml
├─ devmodes.toml
```
{% endstep %}

{% step %}
### Konfigurálás

Szerkeszd a `config.toml` fájlt a saját beállításaid szerint (lásd a Konfiguráció részt).
{% endstep %}

{% step %}
### Konfiguráció újratöltése

Futtasd a következő parancsot játékban vagy konzolon a konfiguráció újratöltéséhez futásidőben:

```
/queuereload
```
{% endstep %}
{% endstepper %}

## Frissítés

Frissítéskor mindig:

{% stepper %}
{% step %}
Állítsd le a proxy-t.
{% endstep %}

{% step %}
Cseréld le a régi `.jar` fájlt az újjal.
{% endstep %}

{% step %}
Indítsd újra a Velocity-t — a konfiguráció és a fejlesztői mód beállításai megmaradnak.
{% endstep %}
{% endstepper %}
