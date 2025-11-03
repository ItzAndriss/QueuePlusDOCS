# Gyakran Ismételt Kérdések

<details>

<summary>Kompatibilis a QueuePlus a BungeeCorddal?</summary>

Nem. A QueuePlus kizárólag **Velocity** proxyhoz készült.

</details>

<details>

<summary>A játékosok automatikusan visszakerülnek a várólistára újraindítás után?</summary>

Igen. Amikor egy szerver újraindul, a QueuePlus automatikusan visszahelyezi a bontott játékosokat a várólistára.

</details>

<details>

<summary>Minden üzenetet testre tudok szabni?</summary>

Igen. Az összes szöveg teljes mértékben konfigurálható a `config.toml` fájl `[messages]` szekciójában.

</details>

<details>

<summary>Hogyan tudom megnézni, mely szerverekhez van várólista?</summary>

A `/queue` parancs automatikus kiegészítése (tab completion) listázza az összes konfigurált szervert.

</details>

<details>

<summary>Mi történik, ha egy szerver végleg offline marad?</summary>

A QueuePlus a játékosokat a várólistán tartja, és az ActionBar üzenetein keresztül értesíti őket, amíg a szerver újra elérhetővé nem válik.

</details>
