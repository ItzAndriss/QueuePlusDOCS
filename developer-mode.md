# Fejlesztői mód

A fejlesztői módot teszteléshez vagy karbantartási időszakokhoz tervezték.\
Amikor aktív, csak a megfelelő jogosultsággal rendelkező játékosok csatlakozhatnak a cél szerverhez.

## Használat

```bash
/queuedev <server> on
```

Csak azok a játékosok csatlakozhatnak, akik rendelkeznek ezzel a jogosultsággal:

```
queue.dev.<server>
```

A kikapcsoláshoz használd:

```bash
/queuedev <server> off
```

## Állapot mentése

A fejlesztői mód állapotai a `plugins/Queue/devmodes.toml` fájlban kerülnek mentésre.\
Ezek az állapotok a proxy újraindítása után is megmaradnak.

## Példa munkafolyamat

{% stepper %}
{% step %}
### Fejlesztői mód engedélyezése frissítés előtt

```bash
/queuedev survival on
```
{% endstep %}

{% step %}
### Indítsd újra a háttérszervert
{% endstep %}

{% step %}
### Teszteld a módosításokat biztonságosan — csak a fejlesztők csatlakozhatnak
{% endstep %}

{% step %}
### Kapcsold ki a fejlesztői módot, ha végeztél

```bash
/queuedev survival off
```
{% endstep %}
{% endstepper %}
