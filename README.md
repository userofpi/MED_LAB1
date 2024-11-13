Oto przykładowy plik `README.md` dla repozytorium zawierającego Twój kod do predykcji liczby użytkowników portalu społecznościowego w oparciu o regresję liniową.

---

# Analiza i Prognoza Liczby Użytkowników Portalu Społecznościowego

Repozytorium zawiera kod w Pythonie do analizy i prognozy liczby użytkowników na podstawie danych historycznych. Kod używa modelu regresji liniowej do przewidywania liczby użytkowników w kolejnych latach oraz tworzy wizualizacje z przedziałami ufności.

## Zawartość repozytorium

- `data.csv`: Plik z danymi historycznymi zawierający liczbę użytkowników i lata.
- `predict_users.py`: Kod Pythona do wczytania danych, trenowania modeli, prognozowania i wizualizacji wyników.
- `README.md`: Instrukcja obsługi i opis działania projektu.

## Opis danych

Dane zawierają kolumny:

- **Rok**: Rok dla danego pomiaru liczby użytkowników.
- **Użytkownicy_mln**: Liczba użytkowników (w milionach) w danym roku.

## Opis działania

### 1. Wczytanie i przygotowanie danych

Kod wczytuje dane z pliku CSV, a następnie dzieli je na zbiór treningowy (lata 2009–2014) oraz testowy (lata 2015–2017).

### 2. Model liniowy na danych pierwotnych

Model liniowy jest trenowany na liczbie użytkowników w latach 2009–2014. Następnie kod oblicza prognozy i przedział ufności dla lat testowych oraz roku 2021.

### 3. Model liniowy na logarytmicznych danych liczby użytkowników

Kod wykonuje transformację logarytmiczną liczby użytkowników, trenuje nowy model i dokonuje prognozy na rok 2021. Transformacja logarytmiczna jest stosowana, aby lepiej dopasować model do danych, które mogą mieć wykładniczy wzrost.

### 4. Wizualizacja wyników

Wyniki są wizualizowane na wykresie, który zawiera:

- Punkty danych rzeczywistych liczby użytkowników.
- Linię regresji oraz przedział ufności dla danych testowych.
- Prognozy na 2021 rok.

## Instrukcje instalacji

1. **Klonowanie repozytorium**:
   ```bash
   git clone https://github.com/yourusername/repo-name.git
   cd repo-name
   ```

2. **Instalacja wymaganych bibliotek**:
   ```bash
   pip install pandas numpy matplotlib scikit-learn scipy
   ```

3. **Uruchomienie kodu**:
   ```bash
   python predict_users.py
   ```

## Wyniki i interpretacja

- **Współczynnik determinacji \( R^2 \)**: Model ocenia dokładność prognozy na danych testowych.
- **Średni błąd predykcyjny**: Średnia różnica między rzeczywistą liczbą użytkowników a wartościami przewidywanymi przez model.
- **Prognoza na 2021 rok**: Przewidywana liczba użytkowników na podstawie modeli liniowego i logarytmicznego.

## Przyszłe kroki

- Dodanie bardziej zaawansowanych metod prognozowania, np. modele nieliniowe.
- Analiza wpływu dodatkowych czynników, takich jak przychody czy zatrudnienie, na prognozy liczby użytkowników.

## Autor

Projekt przygotowany przez Maciej Klimiuk i Hanna Mika.

