# Analiza Testu Bechdel w przemyśle filmowym. Wpływ reprezentacji kobiet na finanse produkcji

## Opis projektu
Projekt to kompleksowe badanie analityczne oparte na danych historycznych z lat 1970–2013, mające na celu zweryfikowanie relacji między reprezentacją kobiet w kinie a finansowym sukcesem produkcji. Wykorzystując Test Bechdel jako narzędzie miary, analiza sprawdza, jak decyzje budżetowe studiów filmowych oraz globalne przychody box office korelują z obecnością i rolą bohaterek na ekranie. 

Dokument udowadnia umiejętność pracy z nieustrukturyzowanymi danymi, przeprowadzania wnioskowania statystycznego oraz przekładania wyników na konkretne wnioski biznesowe i społeczne.

## Zakres analizy
W ramach projektu sformułowano i zbadano cztery kluczowe hipotezy:
1. **Dyskryminacja budżetowa:** Porównanie początkowych budżetów produkcyjnych dla filmów zdających i niezdających Testu Bechdel.
2. **Dynamika historyczna:** Analiza trendów zmian odsetka filmów pozytywnie przechodzących test na przestrzeni czterech dekad.
3. **Struktura niezaliczenia:** Szczegółowa dekompozycja przyczyn, dla których filmy najczęściej oblewają test (brak postaci, brak rozmów, monotematyczność dialogów).
4. **Rentowność i przychody:** Zestawienie globalnych przychodów (skorygowanych o inflację) w celu weryfikacji powszechnego w branży przekonania o wyższej rentowności filmów męskocentrycznych.

## Kluczowe wnioski
* Filmy niezalicząjące Testu Bechdel dysponują średnio o 40% wyższymi budżetami produkcyjnymi na starcie, co wskazuje na zachowawczą strategię inwestycyjną wytwórni.
* Odsetek filmów zdających test rośnie systematycznie, podwajając się na przestrzeni badanych 40 lat (szczyt w dekadzie 2000-2009).
* W ponad 50% przypadków filmy nie zdają testu nie z powodu braku postaci kobiecych na ekranie, lecz z powodu braku jakichkolwiek interakcji dialogowych między nimi.
* Produkcje skupione na mężczyznach generują statystycznie wyższe średnie przychody, jednak analiza wartości odstających i zestawień TOP 10 (np. przypadek "Titanica") udowadnia, że filmy z rozbudowaną reprezentacją kobiet posiadają równie wysoki potencjał komercyjny.

## Źródło i przygotowanie danych
Projekt bazuje na zbiorze `movies.csv` udostępnionym na otwartej licencji przez portal FiveThirtyEight. Zawiera on 1794 unikalne rekordy łączące oceny widzów (Bechdel Test Movie List) z danymi finansowymi (The Numbers). W ramach projektu przeprowadzono czyszczenie danych: standaryzację typów zmiennych, konwersję wartości finansowych, usunięcie braków danych w kluczowych wierszach (NA) oraz kategoryzację wyników na zmienne czynnikowe (factors). Wszystkie kwoty zostały skorygowane o inflację i sprowadzone do wartości dolara z 2013 roku.

## Środowisko i technologie
Projekt został napisany w języku **R** przy użyciu środowiska Quarto/RMarkdown, co pozwala na generowanie powtarzalnych raportów analitycznych.

Wykorzystane pakiety:
* `tidyverse` (`dplyr`, `ggplot2`, `readr`, `tidyr`) - manipulacja danymi, grupowanie oraz tworzenie wykresów.
* `scales` - formatowanie wartości numerycznych na osiach wykresów.
* `knitr`, `kableExtra` - formatowanie i generowanie profesjonalnych tabel w formacie LaTeX.

