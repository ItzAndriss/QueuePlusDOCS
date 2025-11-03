# Bevezetés

A QueuePlus egy modern, teljes funkcionalitású várólista-kezelő plugin, amelyet **Velocity** proxy hálózatokhoz fejlesztettek ki.\
Biztosítja a zökkenőmentes szerverváltást, megakadályozza a játékosok spamelését újraindítás közben, és kezeli a fejlett funkciókat, mint például a fejlesztői mód, a prioritásos várólista és a lobby terheléselosztás.

***

## Miért a QueuePlus?

A hagyományos várólista pluginokkal ellentétben a QueuePlus a következőket nyújtja:

* Valós idejű ActionBar visszajelzés a várólistán lévő játékosoknak
* Automatikus visszahelyezés újraindítás után
* LuckPerms alapú prioritáskezelés
* Fejlesztőknek fenntartott hozzáférés (fejlesztői mód)
* Konfigurálható késleltetés újraindítás után (pl. 30 másodperces bemelegítés)
* Több lobby között terheléselosztás
* Teljesen testreszabható üzenetek a `config.toml` fájlban

***

## Áttekintés

| Funkció            | Leírás                                               |
| ------------------ | ---------------------------------------------------- |
| Okos újra-várólista | Automatikusan visszahelyezi a játékosokat újraindítás után |
| Fejlesztői mód     | Hozzáférés korlátozása karbantartás vagy tesztelés alatt |
| Prioritásos várólista | LuckPerms integráció rang alapú várólistához       |
| Lobby terheléselosztás | A legkevésbé telített lobbyba irányítja a játékost |
| ActionBar frissítések | Valós idejű visszajelzés a pozícióról és állapotról |
| Konfigurálható     | Minden üzenet és időzítés szerkeszthető              |

A QueuePlus úgy lett megtervezve, hogy nagy méretű hálózatokon is éles környezetben, minimális beállítással működjön.
