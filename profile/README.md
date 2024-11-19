[![Build Docker Images](https://github.com/THD-C/The_THDc_App/actions/workflows/build.yml/badge.svg)](https://github.com/THD-C/The_THDc_App/actions/workflows/build.yml)

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

<p float="left">
  <img src="/Pictures/architecture.png" width="45%" />
</p>

- [Frontend](https://github.com/THD-C/Frontend)
- [Frontend API](https://github.com/THD-C/Frontend_API)
- [DB Manager](https://github.com/THD-C/DB_Manager)
- [Price Manager](https://github.com/THD-C/CoinGecko_API)
