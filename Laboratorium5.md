##Laboratorium 5


1\. Znajdź w swoim katalogu *domowym* (bez podkatalogów) wszystkie pliki, które zostały zmodyfikowane w ciągu 
ostatnich dziesięciu dni i wyświetl ich nazwy.
```sh
find ~/ -maxdepth 1 -type f -mtime -10
```

2\. Znajdź wszystkie pliki zwykłe w systemie, które mają w nazwie ciąg znaków *„conf”* i wyświetl ich nazwy na ekranie.
```sh
find / -name *conf* -type f 2> /dev/null
```
