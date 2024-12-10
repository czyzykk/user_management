# README.md

## Dokumentacja Programu Zarządzania Użytkownikami

### Spis treści
1. [Wymagania](#wymagania)
2. [Instalacja](#instalacja)
3. [Używanie programu](#używanie-programu)
    - [Dodawanie użytkownika](#dodawanie-użytkownika)
    - [Edycja użytkownika](#edycja-użytkownika)
    - [Usuwanie użytkownika](#usuwanie-użytkownika)
4. [Walidacja danych użytkownika](#walidacja-danych-użytkownika)
5. [Najlepsze praktyki dotyczące zarządzania danymi użytkowników](#najlepsze-praktyki-dotyczące-zarządzania-danymi-użytkowników)

---

### Wymagania
- Python 3.6 lub nowszy
- Moduły: `json`, `random`, `re`, `os`, `datetime` (wszystkie są standardowo dostępne w Pythonie)

### Instalacja
1. Skopiuj zawartość programu do lokalnego pliku Python, np. `user_management.py`.
2. Upewnij się, że masz zainstalowanego Pythona. Możesz to sprawdzić poprzez uruchomienie komendy:
   ```bash
   python --version
   ```
3. Uruchom program za pomocą:
   ```bash
   python user_management.py
   ```

### Używanie programu

Program umożliwia dodawanie, edytowanie oraz usuwanie użytkowników. Podczas uruchamiania, użytkownik może wybrać, którą akcję chce wykonać.

#### Dodawanie użytkownika
1. Wybierz opcję 1 w menu.
2. Podaj wymagane informacje:
   - ID użytkownika (liczba całkowita)
   - Imię i nazwisko
   - NIP
   - PESEL
   - REGON
   - Adres email
3. Program zweryfikuje wprowadzone dane. W przypadku nieprawidłowego NIP, PESEL lub REGON, zwróci odpowiedni komunikat.

#### Edycja użytkownika
1. Wybierz opcję 2 w menu.
2. Podaj ID użytkownika, którego dane chcesz edytować.
3. Podaj nowe dane (imię i nazwisko oraz adres email).
4. Program zaktualizuje dane użytkownika i potwierdzi.

#### Usuwanie użytkownika
1. Wybierz opcję 3 w menu.
2. Podaj ID użytkownika, którego chcesz usunąć.
3. Program usunie użytkownika i potwierdzi operację.

### Walidacja danych użytkownika
Program wykonuje walidację następujących danych:
- **NIP**: powinien mieć 10 cyfr, jest weryfikowany według wzoru kontrolnego.
- **PESEL**: powinien mieć 11 cyfr, a jego poprawność jest weryfikowana na podstawie daty urodzenia oraz wzoru kontrolnego.
- **REGON**: może mieć 9 lub 14 cyfr. Walidacja odbywa się na podstawie wzoru kontrolnego.

### Najlepsze praktyki dotyczące zarządzania danymi użytkowników
- **Bezpieczeństwo haseł**: Generowane hasła powinny zawierać co najmniej 12 znaków, z wykorzystaniem małych i wielkich liter, cyfr oraz znaków specjalnych. Program nie przechowuje haseł, ale hasła użytkowników powinny być szyfrowane przed zapisaniem do bazy danych.
- **Przechowywanie danych osobowych**: Należy stosować zasady ochrony danych osobowych, w tym przestrzegać przepisów o ochronie danych, takich jak RODO.
- **Minimalizacja danych**: Zbieraj tylko te informacje, które są niezbędne do działania programu.
- **Audyt i kontrola dostępu**: Regularnie monitoruj dostęp do danych oraz wprowadzaj audyty w celu ochrony danych użytkowników.

Zapewnij, że dane użytkowników są przechowywane i przetwarzane w bezpieczny sposób, aby chronić prywatność i bezpieczeństwo osób, których dane dotyczą.
