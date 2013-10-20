## Rozwiązania z bash'a Laboratorium 1

1\. Używając linii poleceń stwórz strukturę katalogów:

```sh
mkdir -p dom praca/{dokumenty,zlecenia/{niezrealizowane,zrealizowane}} nauka/{c,logo,pascal}
tree
.
├── dom
├── nauka
│   ├── c
│   ├── logo
│   └── pascal
└── praca
    ├── dokumenty
    └── zlecenia
        ├── niezrealizowane
        └── zrealizowane

```
2\. Przejdź do katalogu dom i utwórz katalog wazne-sprawy.

```sh
mkdir dom/wazne-sprawy
tree
.
├── dom
│   └── wazne-sprawy
├── nauka
│   ├── c
│   ├── logo
│   └── pascal
└── praca
    ├── dokumenty
    └── zlecenia
        ├── niezrealizowane
        └── zrealizowane
```

3\. Wejdź do katalogu wazne-sprawy i utwórz tam pusty plik rachunki.txt.

```sh
cd dom/wazne-sprawy
touch rachunki.txt
cd ..
tree
.
└── wazne-sprawy
    └── rachunki.txt

```
4\. Będąc w katalogu wazne-sprawy skopiuj plik rachunki.txt do katalogu zrealizowane.
```sh
cp rachunki.txt ../../../temp/praca/zlecenia/zrealizowane/
cd ../..
tree
.
├── dom
│   └── wazne-sprawy
│       └── rachunki.txt
├── nauka
│   ├── c
│   ├── logo
│   └── pascal
└── praca
    ├── dokumenty
    └── zlecenia
        ├── niezrealizowane
        └── zrealizowane
            └── rachunki.txt

```

5\. Przejdź do katalogu zrealizowane i zmień nazwę pliku rachunki.txt na wykonano.txt.
```sh
mv rachunki.txt wykonano.txt
└── temp
    ├── dom
    │   └── wazne-sprawy
    │       └── rachunki.txt
    ├── nauka
    │   ├── c
    │   ├── logo
    │   └── pascal
    └── praca
        ├── dokumenty
        └── zlecenia
            ├── niezrealizowane
            └── zrealizowane
                └── wykonano.txt

```



Polecenia: split, cat, diff


6\. Utwórz plik wykonano.txt wielkości 11 bajtów, następnie podziel go pliki wielkości 5 bajtów. W ten sposób otrzymasz 3 pliki. (split)
```sh
cd praca/zlecenia/zrealizowane/
cat >wykonano.txt
12345678901
^C
split -b 5 wykonano.txt

```
7\. Będąc w katalogu logo skopiuj powyżej otrzymane 3 pliki do katalogu dokumenty.
```sh
```
8\. Będąc w katalogu dokumenty połącz skopiowane 3 pliki w plik odtworzono.txt, tak aby otrzymać plik o zawartości identycznej z wykonano.txt. 
    Następnie plik odtworzono.txt skopiuj do katalogu wazne-sprawy.
```shcal 
```
9\. Będąc w katalogu wazne-sprawy sprawdź, czy są jakieś różnice w zawartości plików wykonano.txt i odtworzono.txt.
```sh
```
10\. Wyświetl kalendarz na październik 2009 r. (cal)
```sh
cal 2009
                            2009
      Styczeń                 Luty                 Marzec         
ni po wt śr cz pi so  ni po wt śr cz pi so  ni po wt śr cz pi so  
             1  2  3   1  2  3  4  5  6  7   1  2  3  4  5  6  7  
 4  5  6  7  8  9 10   8  9 10 11 12 13 14   8  9 10 11 12 13 14  
11 12 13 14 15 16 17  15 16 17 18 19 20 21  15 16 17 18 19 20 21  
18 19 20 21 22 23 24  22 23 24 25 26 27 28  22 23 24 25 26 27 28  
25 26 27 28 29 30 31                        29 30 31              
                                                                  

      Kwiecień                Maj                 Czerwiec        
ni po wt śr cz pi so  ni po wt śr cz pi so  ni po wt śr cz pi so  
          1  2  3  4                  1  2      1  2  3  4  5  6  
 5  6  7  8  9 10 11   3  4  5  6  7  8  9   7  8  9 10 11 12 13  
12 13 14 15 16 17 18  10 11 12 13 14 15 16  14 15 16 17 18 19 20  
19 20 21 22 23 24 25  17 18 19 20 21 22 23  21 22 23 24 25 26 27  
26 27 28 29 30        24 25 26 27 28 29 30  28 29 30              
                      31                                          

       Lipiec               Sierpień              Wrzesień        
ni po wt śr cz pi so  ni po wt śr cz pi so  ni po wt śr cz pi so  
          1  2  3  4                     1         1  2  3  4  5  
 5  6  7  8  9 10 11   2  3  4  5  6  7  8   6  7  8  9 10 11 12  
12 13 14 15 16 17 18   9 10 11 12 13 14 15  13 14 15 16 17 18 19  
19 20 21 22 23 24 25  16 17 18 19 20 21 22  20 21 22 23 24 25 26  
26 27 28 29 30 31     23 24 25 26 27 28 29  27 28 29 30           
                      30 31                                       

    Październik             Listopad              Grudzień        
ni po wt śr cz pi so  ni po wt śr cz pi so  ni po wt śr cz pi so  
             1  2  3   1  2  3  4  5  6  7         1  2  3  4  5  
 4  5  6  7  8  9 10   8  9 10 11 12 13 14   6  7  8  9 10 11 12  
11 12 13 14 15 16 17  15 16 17 18 19 20 21  13 14 15 16 17 18 19  
18 19 20 21 22 23 24  22 23 24 25 26 27 28  20 21 22 23 24 25 26  
25 26 27 28 29 30 31  29 30                 27 28 29 30 31        

```

Wyświetl kalendarz na wrzesień, październik i listopad 2009 r. z miesiącami obok siebie (cal):

```sh
cal 10 2009 -3

   Wrzesień 2009        Październik 2009       Listopad 2009      
ni po wt śr cz pi so  ni po wt śr cz pi so  ni po wt śr cz pi so  
       1  2  3  4  5               1  2  3   1  2  3  4  5  6  7  
 6  7  8  9 10 11 12   4  5  6  7  8  9 10   8  9 10 11 12 13 14  
13 14 15 16 17 18 19  11 12 13 14 15 16 17  15 16 17 18 19 20 21  
20 21 22 23 24 25 26  18 19 20 21 22 23 24  22 23 24 25 26 27 28  
27 28 29 30           25 26 27 28 29 30 31  29 30                 

```
Wyświetl kalendarz na październik, listopad i grudzień 2009 r. w taki sposób:

```sh
cal 11 2009 -3
                            2009
    Październik             Listopad              Grudzień        
ni po wt śr cz pi so  ni po wt śr cz pi so  ni po wt śr cz pi so  
             1  2  3   1  2  3  4  5  6  7         1  2  3  4  5  
 4  5  6  7  8  9 10   8  9 10 11 12 13 14   6  7  8  9 10 11 12  
11 12 13 14 15 16 17  15 16 17 18 19 20 21  13 14 15 16 17 18 19  
18 19 20 21 22 23 24  22 23 24 25 26 27 28  20 21 22 23 24 25 26  
25 26 27 28 29 30 31  29 30                 27 28 29 30 31        
                                                                  

```
I jeszcze raz na wrzesień i październik oraz na październik i listopad 2009 r z miesiącami obok siebie (cal, cut?):

```sh
```
11\. Jaki był dzień tygodnia 25 maja 1975 r. (cal i date)
```sh
```
