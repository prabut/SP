##Laboratorium 4


1\. Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże
```sh
ls -1F | sed -e '/[/]/d' | tr 'a-z' 'A-Z'
```
2\. Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę
```sh
ls -hgoF --full-time | tr -s " " | cut -f 1,3,7 -d " " | sed -e '/[/]/d' | tr " " "\t"
```
3\. Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku
```sh
ls -1lS | sed -e '/^d/d' | tr -s " " | cut -f 5,9 -d " " | tac
```
4\. Wyświetl zawartość pliku */etc/passwd* posortowaną według numerów UID w kolejności od największego do najmniejszego
```sh
cat /etc/passwd | sort -t : -k 3 -nr
```
5\. Wyświetl zawartość pliku */etc/passwd* posortowaną najpierw według numerów GID w kolejności od największego do najmniejszego, a następnie UID
```sh
cat /etc/passwd | sort -t : -k 4 -nr -k 3 -nr
```
6\. Podaj liczbę plików każdego użytkownika
```sh
find -type f -printf "%U\n" | sort | uniq -c | sort
```
7\. Sporządź statystykę praw dostępu (dla każdego z praw dostępu podaj, ile razy zostało ono przydzielone)
```sh
find -type f -printf "%m\n" | sort | uniq -c
```
8\. Czy potrafisz odpowiedzieć jaki będzie efekt wykonania poniższych poleceń?
ls -l > lsout.txt                           #  1
ls -la >> lsout.txt                         #  2
ps >> psout.txt                             #  3
free -m >> ~/wynik                          #  4
kill -1 1234 > killout.txt 2>killerr.txt    #  5
kill -1 1234 > killout.txt 2>&1             #  6
kill -1 1234 > /dev/null 2>&1               #  7
sort psout.txt > pssort.txt                 #  8
ps | sort > pssort.txt                      #  9
cat lsout.txt | sort > lssort.txt           # 10
who | sort | more                           # 11
who | sort | less                           # 12
find -type f | wc                           # 13
find -type f -print0 | wc --files0-from=-   # 14
