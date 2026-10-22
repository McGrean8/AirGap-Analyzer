# 🛡️ AirGap Analyzer

**Przedstawiam Proof of Concept (PoC) projektu AirGap Analyzer.**

Aplikacja przeznaczona jest do zaawansowanej analizy dużych zbiorów danych, ze szczególnym uwzględnieniem wycieków informacji (data leaks). System pozwala na wizualną eksplorację zgromadzonych informacji – analizowane dane pokazywane są w formie interaktywnych **grafów powiązań** oraz **mapy**, z której wynika, z jakich krajów pochodzą badane dane.

Kluczowym elementem systemu jest zaimplementowany **chat bot do zadawania pytań** dotyczących tych danych. Agent AI operuje na zadanym zbiorze, natychmiastowo udzielając precyzyjnych odpowiedzi na polecenia analityka. Do jego budowy wykorzystana została platforma **Ollama** oraz **Agent AI oparty na modelu LLaMA**.

Najważniejszą cechą projektu jest jego architektura bezpieczeństwa: to wszystko działa w **środowisku w pełni lokalnym, odizolowanym od internetu**, co zapewnia analitykom **pełen OPSEC** oraz najwyższy standard bezpieczeństwa – **Air Gap**.

---

## 🎥 Prezentacja Systemu (Skrót)

https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Short.mp4

> **[WIDEO: Zobacz krótkie podsumowanie możliwości systemu]** 

---

## 📸 Funkcjonalności i Moduły

### 1. Dashboard Systemowy i Akwizycja
System przetwarza potężne zbiory danych, automatycznie rozpoznając ich strukturę. Wbudowany, odizolowany skaner oblicza entropię pliku i ocenia poziom zagrożenia (malware) przed dopuszczeniem danych do analizy.

![Dashboard Systemowy](AirGap%20Analyzer-Dashboard.jpg)

### 2. Analiza Przestrzenna (Mapa Geo)
Wizualizacja pochodzenia danych na interaktywnej mapie świata. Moduł pozwala na błyskawiczne zidentyfikowanie geograficznych epicentrów wycieku – wskazując dokładnie, z jakich krajów pochodzą rekordy i gdzie jest ich najwięcej.

https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Mapa.mp4

> **[WIDEO: Przegląd danych na Mapie Geo]**

![Mapa Geo](AirGap%20Analyzer-Mapa-ss.jpg)

### 3. Graf Powiązań
Sieć powiązań wygenerowana na podstawie analizy. Wizualizuje skomplikowane relacje między poszczególnymi osobami, ich lokalizacją oraz wykorzystywanymi domenami (np. gmail.com, hotmail.com). To potężne narzędzie do demaskowania ukrytych sieci powiązań.

https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Graf.mp4

> **[WIDEO: Eksploracja Grafu Powiązań]**

![Graf Powiązań](AirGap%20Analyzer-Graf-ss.jpg)

### 4. Dziennik Aktywności Śledczej (Raportowanie)
Moduł realizujący wymagania informatyki śledczej (Chain of Custody). Generuje kompleksowe raporty logujące sumy kontrolne plików, użyte prompty i zwrócone dane dowodowe. Pozwala również na bezpieczne maskowanie informacji wrażliwych przed eksportem.

https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Raport.mp4

> **[WIDEO: Generowanie Dziennika Operacyjnego]**

---

## 🤖 Agent AI w akcji (Lokalna LLaMA)
Zobacz, jak wbudowany chat bot błyskawicznie radzi sobie z analizą ustrukturyzowanej bazy danych, przyjmując komendy od analityka i dokonując zapytań lokalnie – bez żadnego połączenia z internetem.

https://github.com/McGrean8/AirGap-Analyzer/releases/download/v1.0/AirGap.Analyzer-Chat.mp4

> **[WIDEO: Chat bot AI - Pełny zapis analizy danych]**

---

## ⚙️ Wykorzystane Technologie
- **AI & Przetwarzanie Języka:** Platforma `Ollama`, modele rodziny `LLaMA`
- **Interfejs & Wizualizacje:** `PyQt6`, `Plotly` (Geo Analytics), `PyVis` (Network Graphs)
- **Silnik Bazy Danych:** `DuckDB` (In-Memory Processing)
- **Przetwarzanie Danych:** `Pandas`
