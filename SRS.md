# SRS API aplikace

- Autor: Jakub Černošek
- Verze: 1.0
- Datum: 8.10.2024

## Historie dokumentu
| Verze | Datum | Autor          | Komentář                          |
|-------|-------|--------|-----------------------------------|
| 1.0     | 8.10. |Jakub Černošek    | První verze dokumentu            |
| 1.1     | 4.11. |Jakub Černošek    | Upravení produktu jako celek, přidání funkčních požadavků|
| 1.2     | 8.11. |Jakub Černošek    | Přidání historie verzí a priority požadavků, úprava cílové platformy|
## Úvod
### Účel
- Vytvořit aplikaci, ve které se budou zobrazovat objekty které jsou blízko Zemi.

### Konvence dokumentu
- Hlavní nadpisy jsou označené jako "**#**". Podnadpisy jsou pak označené "**##**" a "**###**". Nížší úrovně jsou už označované "nestováním bullet listů" pomocí znaku "-".

### Cílová skupina
- Cílová skupina jsou lidé, které zajímají novinky ohledně objektů, které se pohybují kolem Země.

### Další informace
- Žádné další informace nejsou

### Kontakty 
- jakub.cernosek1@gmail.com
- +420 799 790 193

### Odkazy na další dokumenty
- Momentálně jiné dokumenty, na které by se dalo odkazovat neexistují.

## Celkový popis
### Produkt jako celek
- Produkt bude funkční aplikace, která bude schopna získávat data z NASA API, pomocí klíče který bude přednastavený anebo uživatelem zvolený.

### Funkce
- Finální aplikace bude schopna zobrazovat detaily ohledně objektů, které se pohybují kolem Země. Více detailů [dole](https://github.com/NewJakub/NASA_API_App/blob/main/SRS.md#vlastnosti-syst%C3%A9mu).

### Uživatelské skupiny
- Uživatelé nebudou rozřazeni do skupin, protože to není nutné - aplikace na to není dostatečně složitá.

### Provozní prostředí
- Mobilní zařízení s operačním systémem Windows.

### Uživatelské prostředí
- **.exe** aplikace s GUI rozhraním.

### Omezení návrhu a implementace
- Není.

### Předpoklady a závislosti
- Velmi málo náročné na hardware. Nutnost připojení k internetu kvůli aktualizaci dat z API.


## Požadavky na rozhraní

### Uživatelská rozhraní
- Uživatelské rozhraní bude aplikace pro Windows. Samotné rozhraní se bude skládat z hlavního menu a nastavení.

### Hardwarová rozhraní
- Není.

### Softwarová rozhraní
- Nutnost operačního systému Windows.


## Vlastnosti systému

### Vlastnost U1 - Hlavní menu
- Popis a důležitost: Hlavní menu bude pro uživatele ta nejdůležitější část této aplikace. Bude se v ní nacházet výčet všech asteroidů a jejich podrobné údaje. Právě zde bude uživatel mít možnost se dostat do nastavení.
- Vstupy – Akce – Výsledek: Nejsou.
- Typ: Funkční požadavek.
- Priorita: Vysoká.
  
### Vlastnost U2 - Nastavení
- Popis a důležitost: Uživatel bude moct pomocí tlačítka v pravém horním rohu přejít do nastavení. 
- Vstupy – Akce – Výsledek: Stisknutí tlačítka uživatelem, změna hlavního menu na nastavení.
- Typ: Funkční požadavek.
- Priorita: Nízká.

### Vlastnost U3 - Změna API klíče
- Popis a důležitost: Uživatel bude mít možnost změnit si API klíč v nastavení. Toho dosáhne tak, že do prázdného textového pole vloží samotný klíč. Pokud bude klíč neplatný, bude na to upozorněn v hlavním menu.
- Vstupy – Akce – Výsledek: Textový vstup od uživatele, změna API klíče, možnost upozornění v případě špatného klíče.
- Typ: Funkční požadavek.
- Priorita: Nízká.
  
### Vlastnost U4 - Zobrazování asteroidů
- Popis a důležitost: V hlavním menu se bude nacházet seznam všech asteroidů, které nám pošle API. Pokud bude uživatel chtít, tak bude mít možnost si rozkliknout jakýkoliv asteroid, který si vybere. Následovně se mu zobrazí všechny jeho detaily, jako jsou: jeho velikost a její porovnání k nějakému předmětu na zemi s podobnou velkostí, jeho rychlost a za jak dlouho by byl schopen obletět Zemi, jestli je nebezpečný a datum přiblížení asteroidu.
- Vstupy – Akce – Výsledek: Zobrazení seznamu asteroidů.
- Typ: Funkční požadavek.
- Priorita: Vysoká.
  
### Vlastnost U5 - Obnovení výsledků
- Popis a důležitost: Pokaždé, co uživatel zapne aplikace, pošleme na API nový požadavek o data. Pokud uživatel nebude mít přístup k datovému připojení, budou použita poslední aktualizovaná data a bude zobrazeno poslední datum aktualizace. Uživatel taky bude mít možnost aktualizovat výsledky sám, pomocí tlačítka v levém horním rohu.  
- Vstupy – Akce – Výsledek: Stisknutí tlačítka uživatelem, aktualizace zobrazovaných dat.
- Typ: Funkční požadavek.
- Priorita: Vysoká.
  
### Vlastnost U6 - Rychlost
- Popis a důležitost: Výkonnost této aplikace záleží na rychlosti odpovědi API, tudíž specifikujeme požadovanou rychlost aplikace bez započítání odpovědi API. To znamená že "response time" nebude delší jak 1 sekunda.  
- Vstupy – Akce – Výsledek: Nejsou.
- Typ: Nefunkční požadavek.
- Priorita: Střední.
  
### Vlastnost U7 - Dokumentace
- Popis a důležitost: Jako dokumentace tohoto projektu budou sloužit tento dokument a v budouvnu dokument SRS.   
- Vstupy – Akce – Výsledek: Nejsou.
- Typ: Nefunkční požadavek.
- Priorita: Nízká.
  
### Vlastnost U8 - Bezpečnost
- Popis a důležitost: Vzhledem k tomu, že naše aplikace nemá žádné citlivé informace, nemá cenu řešit bezpečnost.   
- Vstupy – Akce – Výsledek: Nejsou.
- Typ: Nefunkční požadavek.
- Priorita: Nízká.
  
