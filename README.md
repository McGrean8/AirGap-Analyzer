# 🛡️ AirGap Analyzer

**Projekt AirGap Analyzer - Proof of Concept (PoC)**

Aplikacja przeznaczona jest do zaawansowanej analizy dużych zbiorów danych, ze szczególnym uwzględnieniem wycieków informacji (data leaks). System pozwala na wizualną eksplorację zgromadzonych informacji. Analizowane dane pokazywane są w formie interaktywnych **grafów powiązań** oraz **mapy**, z której wynika, z jakich krajów pochodzą.

Kluczowym elementem systemu jest zaimplementowany **chat bot do zadawania pytań** dotyczących tych danych. Agent AI operuje na zadanym zbiorze, natychmiastowo udzielając precyzyjnych odpowiedzi na polecenia analityka. Do jego budowy wykorzystana została platforma **Ollama** oraz **Agent AI oparty na modelu LLaMA**.

Najważniejszą cechą projektu jest jego architektura bezpieczeństwa: to wszystko działa w **środowisku w pełni lokalnym, odizolowanym od internetu**, co zapewnia analitykom **pełen OPSEC** oraz najwyższy standard bezpieczeństwa – **Air Gap**.

---

## 🎥 Prezentacja Systemu

https://github.com/user-attachments/assets/52359084-cb6c-4be1-8e05-7d962661ae1e

---

## 📸 Funkcjonalności i Moduły

### 1. Dashboard Systemowy i Akwizycja
System przetwarza potężne zbiory danych, automatycznie rozpoznając ich strukturę. Wbudowany, odizolowany skaner oblicza entropię pliku i ocenia poziom zagrożenia (malware) przed dopuszczeniem danych do analizy.

![Dashboard Systemowy](AirGap%20Analyzer-Dashboard.jpg)

### 2. Analiza Przestrzenna (Mapa Geo)
Wizualizacja pochodzenia danych na interaktywnej mapie świata. Moduł pozwala na błyskawiczne zidentyfikowanie geograficznych epicentrów wycieku – wskazując dokładnie, z jakich krajów pochodzą rekordy i gdzie jest ich najwięcej.

![Mapa Geo](AirGap%20Analyzer-Mapa-ss.jpg)

https://github.com/user-attachments/assets/3863ad9d-dcce-48dc-bb05-413b160adcb9

### 3. Graf Powiązań
Sieć powiązań wygenerowana na podstawie analizy. Wizualizuje skomplikowane relacje między poszczególnymi osobami, ich lokalizacją oraz wykorzystywanymi domenami (np. gmail.com, hotmail.com). To potężne narzędzie do demaskowania ukrytych sieci powiązań.

![Graf Powiązań](AirGap%20Analyzer-Graf-ss.jpg)

https://github.com/user-attachments/assets/af9b1a8f-b126-4550-b94b-2a9d638ecb99

### 4. Dziennik Aktywności Śledczej (Raportowanie)
Moduł realizujący wymagania informatyki śledczej (Chain of Custody). Generuje kompleksowe raporty logujące sumy kontrolne plików, użyte prompty i zwrócone dane dowodowe, takie jak zidentyfikowane adresy e-mail, loginy, hasła czy numery IP. Pozwala również na bezpieczne maskowanie informacji wrażliwych przed eksportem.

Pełny wygenerowany dokument z audytem (plik HTML) możesz sprawdzić i pobrać na dysk tutaj: **[📄 ZOBACZ PEŁNY RAPORT ŚLEDCZY](Dziennik_Operacyjny.html)**.

https://github.com/user-attachments/assets/cadead0f-d31d-4c68-bf50-3abffd769b88

---

## 🤖 Agent AI w akcji (Lokalna LLaMA)
Zobacz, jak wbudowany chat bot błyskawicznie radzi sobie z analizą ustrukturyzowanej bazy danych, przyjmując komendy od analityka i dokonując zapytań lokalnie, bez połączenia z internetem.

https://github.com/user-attachments/assets/0e23d96a-1e7b-4721-bebe-237dfc0996e9
---

## ⚙️ Wykorzystane Technologie
- **AI & Przetwarzanie Języka:** Platforma `Ollama`, modele rodziny `LLaMA`
- **Interfejs & Wizualizacje:** `PyQt6`, `Plotly` (Geo Analytics), `PyVis` (Network Graphs)
- **Silnik Bazy Danych:** `DuckDB` (In-Memory Processing)
- **Przetwarzanie Danych:** `Pandas`
