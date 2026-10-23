# 🛡️ AirGap Analyzer

**Przedstawiam Proof of Concept (PoC) projektu AirGap Analyzer.**

Aplikacja przeznaczona jest do zaawansowanej analizy dużych zbiorów danych, ze szczególnym uwzględnieniem wycieków informacji (data leaks). System pozwala na wizualną eksplorację zgromadzonych informacji – analizowane dane pokazywane są w formie interaktywnych **grafów powiązań** oraz **mapy**, z której wynika, z jakich krajów pochodzą badane dane.

Kluczowym elementem systemu jest zaimplementowany **chat bot do zadawania pytań** dotyczących tych danych. Agent AI operuje na zadanym zbiorze, natychmiastowo udzielając precyzyjnych odpowiedzi na polecenia analityka. Do jego budowy wykorzystana została platforma **Ollama** oraz **Agent AI oparty na modelu LLaMA**.

Najważniejszą cechą projektu jest jego architektura bezpieczeństwa: to wszystko działa w **środowisku w pełni lokalnym, odizolowanym od internetu**, co zapewnia analitykom **pełen OPSEC** oraz najwyższy standard bezpieczeństwa – **Air Gap**.

---

## 🎥 Prezentacja Systemu

https://github.com/user-attachments/assets/2b73951d-e8e8-4d9f-9e6a-773411bf559b

> ☝️ **Krótkie podsumowanie możliwości systemu i przepływu analizy.**

---

## 📸 Funkcjonalności i Moduły

### 1. Dashboard Systemowy i Akwizycja
System przetwarza potężne zbiory danych, automatycznie rozpoznając ich strukturę. Wbudowany, odizolowany skaner oblicza entropię pliku i ocenia poziom zagrożenia (malware) przed dopuszczeniem danych do analizy.

![Dashboard Systemowy](AirGap%20Analyzer-Dashboard.jpg)

### 2. Analiza Przestrzenna (Mapa Geo)
Wizualizacja pochodzenia danych na interaktywnej mapie świata. Moduł pozwala na błyskawiczne zidentyfikowanie geograficznych epicentrów wycieku – wskazując dokładnie, z jakich krajów pochodzą rekordy i gdzie jest ich najwięcej.

https://github.com/user-attachments/assets/e24fcdb4-8cf9-4ac3-b3ad-ae7caec7199b

![Mapa Geo](AirGap%20Analyzer-Mapa-ss.jpg)

### 3. Graf Powiązań
Sieć powiązań wygenerowana na podstawie analizy. Wizualizuje skomplikowane relacje między poszczególnymi osobami, ich lokalizacją oraz wykorzystywanymi domenami (np. gmail.com, hotmail.com). To potężne narzędzie do demaskowania ukrytych sieci powiązań.

https://github.com/user-attachments/assets/56d21dbd-745a-40e9-b862-a80505f6f8a1

![Graf Powiązań](AirGap%20Analyzer-Graf-ss.jpg)

### 4. Dziennik Aktywności Śledczej (Raportowanie)
Moduł realizujący wymagania informatyki śledczej (Chain of Custody). Generuje kompleksowe raporty logujące sumy kontrolne plików, użyte prompty i zwrócone dane dowodowe, takie jak zidentyfikowane adresy e-mail, loginy, hasła czy numery IP. Pozwala również na bezpieczne maskowanie informacji wrażliwych przed eksportem.

Pełny wygenerowany dokument z audytem (plik HTML) możesz sprawdzić i pobrać na dysk tutaj: **[📄 ZOBACZ PEŁNY RAPORT ŚLEDCZY](Dziennik_Operacyjny.html)**.

https://github.com/user-attachments/assets/1ffdec7c-9097-4fae-9772-b6ed92b003ca

---

## 🤖 Agent AI w akcji (Lokalna LLaMA)
Zobacz, jak wbudowany chat bot błyskawicznie radzi sobie z analizą ustrukturyzowanej bazy danych, przyjmując komendy od analityka i dokonując zapytań lokalnie – bez żadnego połączenia z internetem.

https://github.com/user-attachments/assets/d89e7df6-b8fb-4d3f-a285-3ea0cc67eb71

---

## ⚙️ Wykorzystane Technologie
- **AI & Przetwarzanie Języka:** Platforma `Ollama`, modele rodziny `LLaMA`
- **Interfejs & Wizualizacje:** `PyQt6`, `Plotly` (Geo Analytics), `PyVis` (Network Graphs)
- **Silnik Bazy Danych:** `DuckDB` (In-Memory Processing)
- **Przetwarzanie Danych:** `Pandas`
