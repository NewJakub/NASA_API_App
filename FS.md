# FS NASA API APLIKACE

- Autor: Jakub Černošek
- Verze 1.0
- Datum: 4.11.2024

## Úvod
### Účel
- Účel dokumentu je detailní popsání funkcí a stavů aplikace.
### Konvence dokumentu
- Hlavní nadpisy jsou označené jako "#". Podnadpisy jsou pak označené "##" a "###". Nížší úrovně jsou už označované "nestováním bullet listů" pomocí znaku "-". 

### Pro koho je dokument určený
- Programátory, vývojář, designery a zákazníky.
### Odkazy na další dokumenty
- [SRS](https://github.com/NewJakub/NASA_API_App/blob/main/SRS.md)

## Scénáře

### Všechny reálné způsoby použití
- Způsob používání je jen jeden z důvodů jednoduchosti aplikace.
  
### Pracovní tok

- Zapnutí aplikace
  - Po zapnutí aplikace se uživateli zobrazí hlavní menu. Zde bude pro uživatele ta nejdůležitější část této aplikace. Bude se v ní nacházet výčet všech asteroidů a jejich podrobné údaje. Právě zde bude uživatel mít možnost se dostat do nastavení.

- Nastavení
  - Po přechodu do nastavení bude možnost změnit si API klíč v nastavení. Toho dosáhne uživatel tak, že do prázdného textového pole vloží samotný klíč. Pokud bude klíč neplatný, bude na to upozorněn v hlavním menu.

- Neplatný API klíč
  - Pokud bude API klíč, který uživatel zadá neplatný, bude na to upozorněn v hlavním menu.

- Obnovení výsledků
  - Pokaždé, co uživatel zapne aplikace, pošleme na API nový požadavek o data. Pokud uživatel nebude mít přístup k datovému připojení, budou použita poslední aktualizovaná data a bude zobrazeno poslední datum aktualizace. Uživatel taky bude mít možnost aktualizovat výsledky sám, pomocí tlačítka v levém horním rohu.

- Detaily asteroidů
  - Pokud si uživatel rozklikne políčko s asteroidem, ukážou se mu jeho detaily. Více specifikací ohledně datailů [zde](https://github.com/NewJakub/NASA_API_App/blob/main/SRS.md#vlastnost-u4---zobrazov%C3%A1n%C3%AD-asteroid%C5%AF).

### Hlavní moduly (samotné obrázky jsou jenom orientační, barvy budou dodělané podle vybraného schéma)
- Hlavní menu
  - Zde se budou nacházet dvě tlačítka ("Nastavení" a "Obnovit výsledky"), které budou umístěné v panelu nahoře. Pod nimi se pak bude nacházet výčet všech asteroidů, které nám API vrátí. 
  - ![](https://github.com/NewJakub/NASA_API_App/blob/main/Images/main.png)
- Nastavení hry
  - Bude obsahovat textové pole, do kterého bude moct uživatel zadat svůj vlastní API klíč.
  - ![](https://github.com/NewJakub/NASA_API_App/blob/main/Images/settings.png)
- Detaily asteroidu
  - Okno se bude skládat z popisu asteroidu, který nám vrátí NASA API.  
  - ![](https://github.com/NewJakub/NASA_API_App/blob/main/Images/details.png)
