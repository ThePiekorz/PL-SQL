W tym folderze znajdują się kody w języku PL/SQL, które pracowały na poniższej bazie

CREATE TABLE MIASTA (NAZWA_MIASTA VARCHAR2(100), ILOSC_OSOB
NUMBER(10), DATA_NALICZENIA DATE, KTORE_NALICZENIE NUMBER(10));

CREATE TABLE OSOBY (ID_OSOBY NUMBER(10) NOT NULL, NAZWISKO
VARCHAR2(30), IMIE VARCHAR2(30), PLEC VARCHAR2(1) NOT NULL, MIASTO
VARCHAR2(100));

Zadanie 1
Utworzyć sekwencję OSOBY_SEQ i trigger OSOBY_TRG związany z tabelą OSOBY, który podczas wstawiania do tabeli bez względu na wartość podaną przez użytkownika w polu ID_OSOBY nada własny numer kolejny z sekwencji, ale w taki sposób by nie naruszyć klucza głównego, gdyby wartość już istniała w tabeli.

Zadanie 2
Utworzyc tryger OSOBY_PLEC_I_NAZWISKO zwiazany z tabela OSOBY, który podczas wstawiania lub modyfikacji sprawdzi, czy w polu PLEC pojawiła się jedna z liter: k,K,m,M. Jeśli nie, to zabroni wstawienia/modyfikacji rekordu zgłaszając błąd o treści: “NIEPOPRAWNE OKRESLONO PLEC”. Jeśli litery będą z dopuszczalnego zbioru, to tryger ten zadba o to, by ostatecznie w tabeli znalazły się wyłącznie duże litery M lub K. Dodatkowo tryger podczas operacji wstawiania i/lub modyfikacji spowoduje, że wartości w polu NAZWISKO będą wpisane począwszy od dużej litery (pozostałe litery małe).



