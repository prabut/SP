##Laboratorium 5


1\. Znajdź w swoim katalogu *domowym* (bez podkatalogów) wszystkie pliki, które zostały zmodyfikowane w ciągu 
ostatnich dziesięciu dni i wyświetl ich nazwy.
```sh
find ~/ -maxdepth 1 -type f -mtime -10
```
