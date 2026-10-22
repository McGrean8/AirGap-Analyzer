# 🛡️ AirGap Analyzer

**Przedstawiam Proof of Concept (PoC) projektu AirGap Analyzer.**

Aplikacja przeznaczona jest do zaawansowanej analizy dużych zbiorów danych, ze szczególnym uwzględnieniem wycieków informacji (data leaks). System pozwala na wizualną eksplorację zgromadzonych informacji – analizowane dane pokazywane są w formie interaktywnych **grafów powiązań** oraz **mapy**, z której wynika, z jakich krajów pochodzą badane dane.

Kluczowym elementem systemu jest zaimplementowany **chat bot do zadawania pytań** dotyczących tych danych. Agent AI operuje na zadanym zbiorze, natychmiastowo udzielając precyzyjnych odpowiedzi na polecenia analityka. Do jego budowy wykorzystana została platforma **Ollama** oraz **Agent AI oparty na modelu LLaMA**.

Najważniejszą cechą projektu jest jego architektura bezpieczeństwa: to wszystko działa w **środowisku w pełni lokalnym, odizolowanym od internetu**, co zapewnia analitykom **pełen OPSEC** oraz najwyższy standard bezpieczeństwa – **Air Gap**.

---

## 🎥 Prezentacja Systemu (Skrót)

[![Dashboard Systemowy](AirGap%20Analyzer-Dashboard.jpg)](https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Short.mp4)
> ☝️ **Kliknij w obrazek powyżej, aby odtworzyć wideo z podsumowaniem możliwości systemu.**

---

## 📸 Funkcjonalności i Moduły

### 1. Dashboard Systemowy i Akwizycja
System przetwarza potężne zbiory danych, automatycznie rozpoznając ich strukturę. Wbudowany, odizolowany skaner oblicza entropię pliku i ocenia poziom zagrożenia (malware) przed dopuszczeniem danych do analizy.

### 2. Analiza Przestrzenna (Mapa Geo)
Wizualizacja pochodzenia danych na interaktywnej mapie świata. Moduł pozwala na błyskawiczne zidentyfikowanie geograficznych epicentrów wycieku – wskazując dokładnie, z jakich krajów pochodzą rekordy i gdzie jest ich najwięcej.

[![Mapa Geo](AirGap%20Analyzer-Mapa-ss.jpg)](https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Mapa.mp4)
> ☝️ **Kliknij w obrazek, aby odtworzyć wideo z przeglądem danych na Mapie Geo.**

### 3. Graf Powiązań
Sieć powiązań wygenerowana na podstawie analizy. Wizualizuje skomplikowane relacje między poszczególnymi osobami, ich lokalizacją oraz wykorzystywanymi domenami (np. gmail.com, hotmail.com). To potężne narzędzie do demaskowania ukrytych sieci powiązań.

[![Graf Powiązań](AirGap%20Analyzer-Graf-ss.jpg)](https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Graf.mp4)
> ☝️ **Kliknij w obrazek, aby odtworzyć wideo z eksploracji Grafu Powiązań.**

### 4. Dziennik Aktywności Śledczej (Raportowanie)
Moduł realizujący wymagania informatyki śledczej (Chain of Custody). Generuje kompleksowe raporty logujące sumy kontrolne plików, użyte prompty i zwrócone dane dowodowe, takie jak zidentyfikowane adresy e-mail, loginy, hasła czy numery IP. Pozwala również na bezpieczne maskowanie informacji wrażliwych przed eksportem.

Pełny wygenerowany dokument z audytem (PDF/HTML) możesz sprawdzić tutaj: **[📄 ZOBACZ PEŁNY RAPORT ŚLEDCZY](https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/Dziennik_Operacyjny.html)**.

[![Dziennik Aktywności](AirGap%20Analyzer-Raport-ss.jpg)](https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Raport.mp4)
> ☝️ **Kliknij w obrazek, aby odtworzyć wideo z generowania Dziennika Operacyjnego.**

---

## 🤖 Agent AI w akcji (Lokalna LLaMA)
Zobacz, jak wbudowany chat bot błyskawicznie radzi sobie z analizą ustrukturyzowanej bazy danych, przyjmując komendy od analityka i dokonując zapytań lokalnie – bez żadnego połączenia z internetem.

**[▶️ KLIKNIJ TUTAJ, ABY ZOBACZYĆ PEŁNY ZAPIS ANALIZY PRZEZ AGENTA AI](https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Chat.mp4)**

---

## ⚙️ Wykorzystane Technologie
- **AI & Przetwarzanie Języka:** Platforma `Ollama`, modele rodziny `LLaMA`
- **Interfejs & Wizualizacje:** `PyQt6`, `Plotly` (Geo Analytics), `PyVis` (Network Graphs)
- **Silnik Bazy Danych:** `DuckDB` (In-Memory Processing)
- **Przetwarzanie Danych:** `Pandas`
