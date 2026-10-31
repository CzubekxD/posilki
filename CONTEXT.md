# Posiłki

Planowanie posiłków pod dietę odciążającą wątrobę. Na razie tylko kolacje.

## Language

**Produkt**:
Pozycja w bazie z wartościami odżywczymi na 100 g. Albo ogólny (np. „brokuł”), albo konkretny ze sklepu (marka i gramatura z etykiety). Dane mają wskazywać kierunek, nie aptekarską dokładność.
_Avoid_: składnik (to użycie produktu w przepisie)

**Jednostka sklepowa**:
Forma, w jakiej produkt kupuje się w sklepie: sztuka, opakowanie (np. kubek skyru, puszka) albo gramy dla produktów sypkich i ważonych. W niej podaje się ilości w przepisie i na liście zakupów.

**Przepis**:
Lista składników (produkt + ilość w jednostce sklepowej) na jedną porcję bazową oraz kroki przygotowania.

**Porcja bazowa**:
Porcja dla Matiego. Punkt odniesienia dla ilości w przepisie.

**Profil porcji**:
Rodzaj osoby jedzącej kolację: Mati, dorosły mężczyzna, kobieta, dziecko 2–4 lata. Przy każdej kolacji zaznacza się, ile porcji każdego profilu. Na start profile mogą mieć ten sam rozmiar; różnice dojdą, gdy się okaże, że są potrzebne.

**Cel optymalizacji**:
Wybrany przycisk określający, pod co liczy się ocena (np. odciążenie wątroby). Każdy cel ma swoje warunki i wagi, oparte na badaniach.

**Ocena**:
Liczba 1–10 dla przepisu, liczona jawnie ze składowych. Każdy aktywny cel optymalizacji ma swoją ocenę; ocena przepisu to ich średnia.

**Ocena tygodnia**:
Średnia ocen kolacji plus osobne **normy tygodniowe** (np. ryba, strączki, orzechy ile razy w tygodniu). Niespełniona norma daje flagę tygodnia.

**Flaga**:
Ostrzeżenie przy przepisie lub tygodniu. Tylko informuje, nie zmienia oceny. **Żółta**: uważaj, przekroczony próg (np. dużo soli). **Czerwona**: produkt lub ilość wyraźnie sprzeczna z celem (np. alkohol, dużo cukru dodanego). Flaga mówi wprost, co ją powoduje i co zrobić, w kolejności od tego, co ma największy wpływ (Pareto).

**Wskazówka tygodnia**:
Konkretna informacja, czego unikać poza planem w danym tygodniu, wynikająca z tego, co już jest w kolacjach (np. „kolacje mają w tym tygodniu dużo soli z konserw: odpuść wędliny i słone przekąski”). Liczona tylko z planu; to obraz testowy, nie ocena całej diety.

**Szacunek**:
Wartości produktu wpisane przez Claude z pierwszego wyszukiwania w internecie, gdy nie ma jeszcze etykiety. Zawsze widocznie oznaczone, do podmiany na dane z etykiety.

**Opinia**:
Ocena dania przez Matiego po zjedzeniu: podeszło albo nie. Osobna od **oceny** dietetycznej.

**Archiwum**:
Plany z 4 ostatnich tygodni, z oceną i opinią każdego dania. Starsze wypadają.

**Dania OK** / **Dania nie OK**:
Biblioteka przepisów w repo, podzielona według opinii. Dania OK to instrukcje, z których układa się kolejne tygodnie. Dania nie OK zostają zapisane, żeby można je było przywołać albo świadomie pominąć.

**Batch**:
Baza przygotowywana raz (np. kurczak z warzywami w jednym naczyniu) na kilka kolacji.

## Relationships

- **Przepis** składa się z **produktów** w **jednostkach sklepowych**
- **Kolacja** w planie = **przepis** + liczba porcji per **profil porcji**
- **Ocena** i **flagi** zależą od aktywnych **celów optymalizacji**, wybieranych raz dla całego planu
- Wartości odżywcze: domyślnie krótka lista (zależna od celu), pełna lista wszystkiego z etykiety po rozwinięciu
