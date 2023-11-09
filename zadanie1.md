## Zadanie

Polecenia wykonywane w celu rozwiązania każdego zadania zapisuj w pliku
tekstowym.

1. W dowolnym, stworzonym przez siebie, katalogu utwórz następującą strukturę
   katalogów i plików:
```
.
├── mieszkanie
└── podworko
├── brzoza.txt
├── dom
│   ├── kot.txt
│   └── szafa.txt
└── pies.txt
```

2. Wypełnij pliki tekstowe zawartością, przekierowując do nich standardowe
   wyjścia dowolnych poleceń. Plik *kot.txt* wypełnij wyjściem błędu dowolnego
   programu, bo koty są dziwne. Zadbaj, by w każdym pliku znalazło się co
   najmniej 5 linijek.

3. W pośpiechu postanawiasz zabrać jedynie część swoich rzeczy z szafy. Stwórz
   plik *potrzebne.txt*, w którym znajdzie się zawartość *szafa.txt*, z
   pominięciem dwóch linijek z początku i końca. Zrób to przy pomocy dokładnie
   **jednego polecenia**.
<details><summary>Przykład</summary>

Plik *szafa.txt*:

```
buty
spodnie
koszule
mleko
swetry
```

Plik *potrzebne.txt*:

```
koszule
```

</details>

<details><summary>Podpowiedź</summary>
Skorzystaj z odpowiedniego połączenia poleceń `head` i `tail`.
</details>

4. Zapoznaj się z obsługą programu `tar`; skorzystaj z podręcznika systemowego.
   Zwróć szczególną uwagę na przełączniki: `-z`, `-f`, `-c`, `-x`, `-t`. Zanim
   kontynuujesz, przetestuj działanie programu w katalogu */tmp*.

5. Używając programu `tar` przygotuj się do przeprowadzki. Spakuj potrzebne
   rzeczy oraz kota do pliku *walizka.tar.gz*. Przy pomocy **jednego polecenia**
   przenieś walizkę do katalogu *mieszkanie*.

6. Pora się rozpakować. Wypakuj archiwum *walizka.tar.gz*. Następnie wylistuj
   jego zawartość, by upewnić się, że wszystko poszło zgodnie z planem.

7. Zadbaj o bezpieczeństwo! Zmodyfikuj uprawnienia do katalogu *mieszkanie*
   tak, aby użytkownicy spoza twojej grupy nie mogli dostać się do środka.

8. Byś mógł szybciej odwiedzać swojego psa, stwórz **względne** dowiązanie
   symboliczne *mieszkanie/teleport*, wskazujące na katalog *podworko*.

9. Przy pomocy teleportu zdalnie nakarm swojego psa. Korzystając z dowiązania
   *teleport* dopisz na koniec *pies.txt* `NAKARMIONY`.

10. Pora przenieść resztę rzeczy. Utwórz twarde dowiązanie *nowa_szafa*,
    wskazujące na plik *podworko/dom/szafa.txt*.


<details><summary>Struktura katalogów po wykonaniu wszystkich zadań.</summary>

```
[drwxr-xr-x]  .
├── [drwxr-x---]  mieszkanie
│   ├── [-rw-r--r--]  kot.txt
│   ├── [-rw-r--r--]  nowa_szafa
│   ├── [-rw-r--r--]  potrzebne.txt
│   ├── [lrwxrwxrwx]  teleport -> ../podworko
│   └── [-rw-r--r--]  walizka.tar.gz
└── [drwxr-xr-x]  podworko
    ├── [-rw-r--r--]  brzoza.txt
    ├── [drwxr-xr-x]  dom
    │   ├── [-rw-r--r--]  kot.txt
    │   ├── [-rw-r--r--]  potrzebne.txt
    │   └── [-rw-r--r--]  szafa.txt
    └── [-rw-r--r--]  pies.txt
```

</details>
