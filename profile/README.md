![Vercel Deploy](https://deploy-badge.vercel.app/vercel/backend-liard-one?name=Backend)

Appka do trading'u kryptowalut, rodzaj trenera, 
który pobiera rzeczywiste ceny poszczególnych kryptowalut i pozwala użytkownikowi podejmować decyzje o zakupie, sprzedaży.

# Key points
1. Autoryzacja z wykorzystaniem zewnętrznych serwisów:
   - Google
   - Microsoft
   - Facebook
2. Wymogi formalno-prawne:
   - Regulamin
   - RODO
   - akceptacja o Cookies, jeśli są
3. Otwieranie rachunków w różnych walutach
4. Kupowanie sprzedawanie instrumentów (zlecenia instant i pending)
5. Historia operacji na kontach (wpłaty wypłaty)
6. Historia transakcji (sprzedane, kupione)
7. Wykresy cen, pozyskanych z zewnętrznych usług
8. Zamiana walut, żeby można było mieć aplikacje w PLN, USD, EUR
9. Mechanizm promocji i prowizji:
    - do kwoty X, prowizja wynosi 0%
    - powyżej kwoty X, prowizja wynosi Y%
10. Statystyki konta:
    - Maksymalny zysk/strata, w różnych okresach w czasie:
        - ostatni dzień
        - ostatni tydzień
        - ostatni miesiąc
        - ostatni rok
    - Udział procentowy danego instrumentu w całym koncie.
11. Podłączenie do zewnętrznych API.

# Technologie
## Docker
### Baza danych
PostgreSQL - Tabele definiowane przy użyciu SQLAlchemy
### Frontend
SCSS + Tailwind + React
### Backend
Python + FastAPI

![image](/Pictures/architecture.png)
![image](/Pictures/database.png)

# SQL Database
## Tabele
1. Użytkownicy:
    - username
    - password
    - dane osobowe
    - user_id
2. Transakcje:
    - data
    - rodzaj operacji (wpłata/wypłata)
    - waluta
    - kwota
    - user_id
3. Transakcje giełdowe:
    - data (jeżeli transakcja zrealizowana to ma datę, jeśli czeka to data jest NULL)
    - kryptowaluta
    - kwota
    - kurs 
    - user_id
    - rodzaj operacji (instant, stop loss, take profit)
4. Wallet ( wynika z tab. nr 3)
    - ilosc_crypto
    - crypto_id
    - user_id
5. Rachunki/Salda fiat ( wynika z tab. nr 2)
    - ilosc_pieniedzy
    - waluta_id
    - user_id
6. Zlecenia

# No SQL Database
1. Template stron z translacjami (strona główna, rodo, strona z wykresem krypto (niezależne od waluty), do długich tekstów)
    - id strony
    - język
    - tytuł z headera
    - treść
