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

### Hlavní moduly (samotné obrázky jsou jenom orientační, barvy budou dodělané podle vybraného schéma)
- Hlavní menu
  - Zde se budou nacházet dvě tlačítka ("Nastavení" a "Obnovit výsledky"), které budou umístěné uprostřed okna.  
  - ![](https://github.com/NewJakub/NASA_API_App/blob/main/Images/main.png)
- Nastavení hry
  - Bude obsahovat dvě dropdown menu ("Barva" a "Časovač") a jedno tlačítko (Zapnout hru).
  - ![](https://github.com/NewJakub/NASA_API_App/blob/main/Images/settings.png)
- Okno pozastavení hry
  - Okno se bude skládat ze dvou tlačítek ("Vrátit se do hry" a "Opustit aplikaci"), které budou uprostřed obrazovky.  
  - ![](https://github.com/NewJakub/NASA_API_App/blob/main/Images/details.png)
