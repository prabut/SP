## Laboratorium2

W katalogu c utwórz plik program.c zawierający co najmniej 10 linii kodu napisanego w języku C. (Sam kod należy wyszukać i pobrać z sieci.)

```sh
/**********************************************************************************************
 * Program kwad_sumy.c oblicza sume kwadratow n wyrazow. Liczba n jest podawana z klawiatury. *
 * n nalezy do liczb naturalnych.                                                             *
 **********************************************************************************************/

#include <stdio.h>
                int main()
                {
                 int n, suma;
                 printf("\n\nPodaj liczbę n: ");
                 scanf("%d",&n);
                 suma=((n*(n+1))*((2*n)+1))/6;
                 printf("Suma kwadratow liczby %d wynosi: %d\n\n",n,suma);
                 return 0;
                }


```


1\. Wyświetl na ekran 2 pierwsze wiersze pliku program.c. (head)
```sh
head -n 2 kwad_sumy.c 

/**********************************************************************************************
 * Program kwad_sumy.c oblicza sume kwadratow n wyrazow. Liczba n jest podawana z klawiatury. *

```

2\. Wyświetl na ekran 4 ostatnie wiersze pliku program.c. (head, tail)
```sh
tail -n 4 kwad_sumy.c

		 suma=((n*(n+1))*((2*n)+1))/6;
		 printf("Suma kwadratow liczby %d wynosi: %d\n\n",n,suma);
		 return 0;
		}
		
```

3\. W pliku program.c znajdź wszystkie wiersze z wystąpieniem słowa „main”. (grep)
```sh
grep main kwad_sumy.c

int main()
```

4\. Plikowi program.c nadaj następujące uprawnienia: właściciel – czytanie, pisanie, grupa – czytanie, 
    pozostali użytkownicy: brak uprawnień. (chmod)
```sh
chmod 640 kwad_sumy.c 
ls -l
-rw-r----- 1 tprabucki studinf 556 paź 21 15:33 kwad_sumy.c

```

5\. Będąc w katalogu temp przenieś katalog wazne-sprawy do katalogu praca.
```sh

```

6\. Zarchiwizuj cały katalog temp. (zip i tar)
```sh

```

7\. Usuń katalog temp.
```sh

```

8\. Odtwórz z archiwum katalog temp. (unzip i tar)
```sh

```

9\. Posprzątaj na swoim koncie.
```sh

```