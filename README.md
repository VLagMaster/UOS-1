# UOS
## Prvotní info:
* case sensitive (záleží na velikosti písmen)
* příkazy oddělené novou řádkou či středníkem ```;```
* pracujeme uvnitř shellu bash
* záleží na mezerách/tabulátorech
## Časté chybové hlášky bashe
* ```Command not found``` bash nenašel spustitelný soubor v PATHu
* ```No such file or directory``` soubor nebyl nalezen
* ```Permission denied``` soubor existuje ale nemáme k němu oprávnění
## Pohyb po příkazové řádce
* ```šipky``` pohyb v historii shellu (předchozích příkazích)
* ```enter``` odeslání příkazu
* ```tabulátor``` doplnění jmen
* ```CTRL + R``` vyhledání textu v historii
## Příkazy:
### Struktura:
* ```příkaz``` vždy na zečátku
  * může být specifikovaný bez cesty (najde se v ```$PATH```), s absolutní cestou (začíná ```/```), s relativní cestou (vůči tomu, kde se nacházíme), nebo build-in v shellu
* ```přepínaće``` odděleny mezerou
  * ```krátký přepínač``` jedna pomlčka + jeden znak, např. ```-a```
  * ```dlouhý pŕepínač``` dvě pomlčky + slovo, např. ```--verbose```
* ```argumenty``` odděleny mezerou, vstup od uživatele
* speciální znaky
  * ```?``` jeden jakýkoliv znak
  * ```*``` jakýkoliv počet jakýkoliv znaků
### Seznam:
* ```id``` vrátí UID uživatele a skupin
* ```uname``` vrátí systémové informace
  * ```-a``` vrátí vśechny informace
* ```who``` ukáže, kdo je přihlášen
  * ```am i``` ukáže to pouze informace o mě
* ```whoami``` vrátí uživatelské jméno
* ```tty``` vrátí, jaký terminál uživatel používá
* ```cd``` změní složku, ve které se shell nachází
* ```ls``` vypíše obsah adresáře
  * ```-l``` dlouhý výstup, podrobnější
  * ```-a``` vypíše všechny skryté soubory
  * ```-h``` vypíše v lidsky čitelných jednotkách
  * ```-d``` vypíše adresář
  * ```-w``` určí šířku výstupu
* ```declare```
  * ```-p``` vypíše informace o proměnné
* ```type``` ukáže, jak bude shell interpretovat příkaz
* ```tr``` přeloží/smaže znaky
* ```sort``` seŘadí soubor podle řádku
* ```(())``` aritmetické operace v Bashi
* ```read``` čte ze standartního vstupu, pro změnu oddělovače je třeba změnit Proměnnou IFS
* ```awk``` pattern scanning
  * ```awk -F " " '{printf $2 "\n"}'```
  * ```-F``` použije jinný oddělovač
  * ```-v``` zadání
  * ```awk -F 'Oddělovač' -v parametry 'příkaz' soubor
    * např. ```awk -v col=7 '{print $col}' file```
* ```cut```
* ```uniq```
* ```grep ^.......$``` vypíše prvních 7 znaků
* ```unset``` zruší proměnou
* ```test``` check file types and compare values
