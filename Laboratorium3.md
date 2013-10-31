##Laboratorium 3

1\. Wyświetl plik */etc/passwd* z podziałem na strony przyjmując, że strona na 5 linii tekstu. (raczej more niż less)

```sh
more -5 /etc/passwd

root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/bin/sh
bin:x:2:2:bin:/bin:/bin/sh
sys:x:3:3:sys:/dev:/bin/sh
sync:x:4:65534:sync:/bin:/bin/sync
```

2\. Korzystając z polecenia cat utwórz plik *tekst3.txt*, który będzie składał się z zawartości pliku *tekst1.txt*, ciągu znaków podanego ze standardowego wejścia (klawiatury) i pliku *tekst2.txt*.

3\. Wyświetl po 5 pierwszych linii wszystkich plików w swoim katalogu domowym w taki sposób, aby nie były wyświetlane ich nazwy.

4\. Wyświetl linie o numerach 3, 4 i 5 z pliku */etc/passwd*.

5\. Wyświetl linie o numerach 7, 6 i 5 od końca pliku */etc/passwd*.

6\. Wyświetl zawartość pliku */etc/passwd* w jednej linii.

7\. Za pomocą *filtru tr* wykonaj modyfikację pliku *plik.txt*, polegającą na umieszczeniu każdego słowa w osobnej linii.

8\. Zlicz wszystkie pliki znajdujące się w katalogu */etc* i jego podkatalogach.

9\. Napisać polecenie zliczające ilość znaków z pierwszych trzech linii pliku */etc/passwd*.