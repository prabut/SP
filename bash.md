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
4\. Przejdź do katalogu dom i utwórz katalog wazne-sprawy.

```sh
cd ...
```
