# 🎯 QuizApp

**Autor:** Maksym Krytskyi
**Framework:** ASP.NET Core 8.0
**Baza danych:** SQLite
**Frontend:** HTML5, CSS3, Bootstrap 5, JavaScript
**Architektura:** MVC

## 📝 Opis

**QuizApp** to webowa aplikacja do tworzenia, zarządzania i rozwiązywania quizów. Umożliwia użytkownikom:

* Tworzenie własnych quizów z pytaniami wielokrotnego wyboru
* Udostępnianie quizów innym użytkownikom
* Śledzenie wyników i statystyk

## 🚀 Szybki Start

### 1. Klonowanie repozytorium

```bash
git clone [url-repozytorium]
cd QuizApp
```

### 2. Przywrócenie pakietów

```bash
dotnet restore
```

### 3. Utworzenie bazy danych

```bash
dotnet ef database update
```

### 4. Uruchomienie aplikacji

```bash
dotnet run
```

### 5. Przeglądanie aplikacji

```
https://localhost:5001
```

---

## 🗂 Struktura Projektu

```
QuizApp/
├── Controllers/         # Kontrolery MVC
├── Models/              # Modele danych
├── Views/               # Widoki Razor
│   ├── Shared/
│   ├── Home/
│   ├── Quizy/
│   ├── Pytania/
│   ├── Odpowiedzi/
│   ├── WykonajQuiz/
│   └── Statystyki/
├── Data/                # Kontekst EF Core
├── Migrations/          # Migracje EF
├── wwwroot/             # Zasoby statyczne
└── Program.cs           # Główny punkt wejścia
```

---

## 🧩 Główne Funkcje

### ✅ Tworzenie pytań z odpowiedziami

* Dynamiczne dodawanie odpowiedzi (JavaScript)
* Walidacja po stronie klienta i serwera

### ✅ Rozwiązywanie quizów

* Przechowywanie sesji
* Obliczanie wyniku w czasie rzeczywistym
* Blokada cofania się do poprzednich pytań

### ✅ Statystyki

* Średnie wyniki, liczba wypełnień
* Popularność odpowiedzi
* Wizualizacja danych (progress bary, kolorowe karty)

### ✅ Autoryzacja i bezpieczeństwo

* Tylko właściciel może edytować/usunąć swoje quizy
* Walidacja dostępu na poziomie kontrolera
* Ukrywanie danych innych użytkowników

### ✅ Responsywny interfejs

* Działa na desktopie i mobile
* Interaktywne elementy (hover, animacje, breadcrumbs)

---

## 📊 Modele Danych (skrótowo)

| Model                  | Kluczowe pola                 |
| ---------------------- | ----------------------------- |
| `ApplicationUser`      | Imię, Nazwisko, Quizy, Wyniki |
| `Quiz`                 | Tytuł, Opis, Autor, Pytania   |
| `Pytanie`              | Treść, Punkty, Odpowiedzi     |
| `Odpowiedz`            | Treść, CzyPoprawna            |
| `WynikQuizu`           | Użytkownik, Punkty, Procent   |
| `OdpowiedzUzytkownika` | Wybrana odpowiedź             |

Pełny opis modeli znajdziesz w pliku `/Models`.

---

## 🧑‍💻 Użytkownicy i Role

| Typ użytkownika | Uprawnienia                                                              |
| --------------- | ------------------------------------------------------------------------ |
| Gość            | Przeglądanie strony głównej, rejestracja                                 |
| Zalogowany      | Tworzenie quizów, rozwiązywanie quizów, przeglądanie wyników i statystyk |

🔐 **Brak systemu ról – wszyscy użytkownicy mają te same możliwości.**

---

## 📂 Kontrolery

| Kontroler               | Opis                                 |
| ----------------------- | ------------------------------------ |
| `HomeController`        | Strona główna i polityka prywatności |
| `QuizyController`       | Zarządzanie quizami                  |
| `PytaniaController`     | Dodawanie i edycja pytań             |
| `OdpowiedziController`  | Tworzenie odpowiedzi                 |
| `WykonajQuizController` | Rozwiązywanie quizów                 |
| `StatystykiController`  | Podgląd wyników i analiz             |

---

## 🔒 Walidacja i Feedback

* Walidacja formularzy (klient + serwer)
* Sprawdzanie unikalności tytułów quizów
* Komunikaty po operacjach (sukces/błąd)
* Potwierdzenia przed usuwaniem

---

## 🛠 Technologie

* ASP.NET Core 8.0
* Entity Framework Core
* ASP.NET Core Identity
* Bootstrap 5
* SQLite

---

## 📌 Wymagania

* [.NET 8 SDK](https://dotnet.microsoft.com/download)
* Przeglądarka wspierająca HTTPS
* (opcjonalnie) Visual Studio 2022+ lub VS Code

---

## 📬 Kontakt

Masz pytania, uwagi lub chcesz współtworzyć projekt?
Napisz do mnie: **[maksym.krytskyi@example.com](mailto:maksym.krytskyi@example.com)**

---

### ⭐️ Jeśli Ci się podoba, zostaw gwiazdkę repozytorium!

---

Chcesz też dodać badge GitHub Actions, licencję MIT lub zrzuty ekranu? Daj znać — mogę to dorzucić.
