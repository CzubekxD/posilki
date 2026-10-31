# Posiłki — specyfikacja

## Cel
Planowanie posiłków pod dietę odciążającą wątrobę (śródziemnomorska: chude białko, ryby, warzywa, pełne ziarno, zdrowe tłuszcze; bez alkoholu, cukru, smażenia w głębokim tłuszczu, tłustego mięsa i nabiału).

## Zakres — etapy
1. **Teraz: tylko kolacje.** Testujemy proces planowania na 7 kolacjach tygodniowo.
2. Później: kolejne posiłki (śniadania, obiady, przekąski), dodawane po kolei, gdy proces kolacji się sprawdzi.

## Rytm
- Cotygodniowe spotkanie: przegląd tygodnia (co zjedzone, co odpuszczone, co smakowało), nowy plan, lista zakupów.
- Zakupy w Biedronce (Rudzica, lada tradycyjna). Jajka i pieczywo kupowane gdzie indziej — nie trafiają na listę.

## Zasady planu
- Gotowanie w batchach: jedna baza (np. kurczak + warzywa w jednym naczyniu żaroodpornym) na kilka kolacji.
- Pieczywo: bułki razowe/grahamki zamiast bochenka (nie wysychają).
- Ilości w przepisach na 1 osobę, skalowane liczbą osób przy każdej kolacji.
- Produkty z domu (konserwy, cebula) oznaczone i pomijane na liście zakupów.

## Strona planu (`index.html`)
- Belka u góry: ocena całego tygodnia, kolacje zaplanowane/zjedzone, średnie makro.
- Kolacje numerowane 1–7, każda z: liczbą osób (−/+), składnikami, kcal, makro, mikro, oceną 1–10 z uzasadnieniem, checkboxem „zjedzone”.
- Batche z łącznymi ilościami przeliczanymi z kolacji.
- Lista zakupów generowana z przepisów, z checkboxami.

## Dane żywieniowe (następny krok)
- `foods/` — jeden plik na produkt, wartości na 100 g (kcal, B/T/W, błonnik, cukry, cukry dodane, nasycone, sól, omega-3, wybrane mikro) + źródło (etykieta, Open Food Facts, USDA).
- `recipes/` — przepisy jako lista składników w gramach z odwołaniem do `foods/`, bez ręcznie wpisanych wartości.
- `plan/RRRR-TT.yaml` — wybór 7 przepisów na tydzień.
- Skrypt generuje `index.html`: liczy wartości ze składników i ocenę z jawnych składowych (cukier dodany, nasycone, sól, błonnik, omega-3, przetworzenie).

Obecne wartości w `index.html` są szacunkami (±15%) — do zastąpienia wyliczeniami z `foods/`.
