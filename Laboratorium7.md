##Laboratorium 7

1\. W bieżącym katalogu zamienić rozszerzenia wszystkich plików z rozszerzeniem htm na html. 
   Jeżeli w nazwie pliku istnieje spacja, to należy zamienić ją na znak podkreślenia.
```sh
#!/bin/bash
for a in *.htm; 
 do mv $a `basename $a .htm`.html;
done
```
   
2\. Napisać skrypt zawierający funkcję obliczającą silnię. Następnie należy obliczyć silnię z liczby, 
   która jest argumentem skryptu. W przypadku niepoprawnego argumentu należy wypisać odpowiedni komunikat.
```sh

```

3\. Napisać skrypt zbierający jak najwięcej informacji o użytkowniku, którego login jest argumentem skryptu. 
    Jeżeli skrypt nie ma argumentu, to należy użyć login osoby uruchamiającej skrypt.
```sh

```
4\. Napisz skrypt usuwający z katalogu domowego i jego podkatalogów wszystkie pliki zwykłe o nazwie 
   'core' starsze niż 3 dni.
```sh
