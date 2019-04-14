# OSY DU 01

 ## Čtení vstupu řádek po řádku
 ```
 while read line
 do
    echo "Radek: $line"
 done < /dev/stdin
 ```
 ## [Parsování parametrů programu](https://stackoverflow.com/q/192249/607407)
 ## Pole
 Vytvoření nového pole:
 ```
 pole=()
 ```
 Přidání prvku do pole:
 ```
 pole+=("prvek")
 ```
 Pole jako argumenty příkazu:
 ```
 prikaz "${pole[@]}"
 ```
 Délka pole:
 ```
delka=${#pole[@]}
 ```
 ## Počet řádků v souboru
 ```
 wc -l < "cesta k souboru"
 ```
 
 ## První řádek souboru
 ```
 head -n 1 "nazev souboru"
 ```
 ## Cesta k cíli odkazu
 ```
 readlink "cesta k odkazu"
 ```
 ## Kontrola souboru
 Pozor: symbolický odkaz je i soubor. Kontrolujte nejdřív, zda je na cestě odkaz, a teprve pokud není, kontrolujte, zda je to soubor.
 ### Je složka?
 ```
 if [ -d "$filename" ]; then
 ```
 ### Je odkaz?
 ```
 if [ -h "$filename" ]; then
 ```
 ### Je soubor?
 ```
 if [ -f "$filename" ]; then
 ```
 ## Aritmetika
 Aritmetické operace patří do `(( ))`. Nepoužívá se v nich `$`.
 ### Inkrement
 ```
 ((++promenna))
 ```
 ### Rovnost
 ```
 if (( promenna == 0 )); then
 ```
 
 
 
