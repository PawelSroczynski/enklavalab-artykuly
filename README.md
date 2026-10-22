# EnklavaLab — biblioteka artykułów (zgazowanie, biowęgiel, retorty)

Paczka literatury pobranej 22.10.2026 na potrzeby projektu EnklavaLab: zgazowanie biomasy,
silniki na gaz generatorowy, smoła i jej redukcja, reaktywność węgla drzewnego,
retorty i produkcja biowęgla, biowęgiel z fekaliów i osadów.

Zawartość: **25 pozycji zweryfikowanych** (24 PDF-y + folder offline FAO) z 36
przewidzianych na listach A i B. Pozycje z listy „od znajomego" (P01–P33) nie
zostały dostarczone, dlatego ich nie ma.

## Struktura

- `G/` — zgazowanie, silnik, smoła, rozruch
- `R/` — reaktywność węgla, popiół, żużel
- `B/` — retorty, biowęgiel, kompost, fekalia
- `ARTICLES.md` — spis wszystkich pozycji z linkami i statusami
- `MANIFEST.csv` — metadane: plik, grupa, status, źródło, bajty, strony, sha256, uwagi
- `nieudane.txt` — pozycje do otwarcia ręcznie w przeglądarce

## Skąd pliki

Wyłącznie z adresów podanych w instrukcji zlecenia albo z linków na tych stronach.
Bez Sci-Hub, LibGen, Anny's Archive i bez nieoficjalnych kopii. Bez logowania,
bez rozwiązywania CAPTCHA. Żądania rozłożone w czasie (2–3 s przerwy, max 2 ponowienia).

Część wydawców (MDPI, Springer, Akamai) blokuje `curl` kodem 403 — te pliki
pobrano przez realną przeglądarkę (Chromium/Puppeteer).

## Jak weryfikowano

Każdy plik musi przejść cztery warunki: nagłówek `%PDF`, rozmiar > 50 kB,
`pdfinfo` zgłasza ≥ 2 strony, a tekst pierwszych trzech stron zawiera słowo
kontrolne przypisane do pozycji. Pliki bez warstwy tekstowej (skany) mają status
`SKAN` i zostają w paczce.

## Statusy

| status | znaczenie |
|---|---|
| OK | pobrane i zweryfikowane |
| SKAN | poprawny PDF bez tekstu (skan) |
| NIEUDANE | 403, brak DNS, HTML zamiast PDF, brak słowa kontrolnego |
| POMINIĘTE | wymaga logowania |
| ZAMKNIĘTE | wydawca nie udostępnia PDF bez opłaty |
| BRAK | pozycja z listy „od znajomego", niedostarczona |

## Prawa autorskie

Pliki nie są moje i nie są tu objęte żadną moją licencją. Pochodzą z serwisów
wydawców i repozytoriów uczelnianych; prawa należą do autorów i wydawców.
Część jest na licencjach otwartych (CC BY), część to kopie ze stron autorów lub
rozprawy z repozytoriów instytucjonalnych, część nie ma zgody na redystrybucję.
Repozytorium ma charakter roboczy, wewnętrzny — nie jest oficjalnym archiwum
i nie służy do ponownego rozpowszechniania. Jeśli jesteś autorem lub wydawcą
i chcesz usunięcia pliku, otwórz issue — plik zniknie.

## Odtworzenie

Skrypty użyte do pobrania i weryfikacji: `fetch.py`, `retry.py`, `pwfetch*.js`,
`finalize.py` (poza tym repozytorium — w katalogu roboczym projektu).
