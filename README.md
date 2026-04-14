# dbuczynski's Home Assistant Integrations

To repozytorium to zbiór autorskich, niestandardowych integracji dla środowiska Home Assistant, gotowy do łatwego wdrożenia poprzez **HACS** (Home Assistant Community Store).

## 📦 Lista Integracji

W obecnej paczce do katalogu Twojego serwera zostaną pobrane następujące wtyczki:

### 1. Galeria Twarzy (`galeria_twarzy`)
Integracja typu Web Scraper z wbudowanym mechanizmem pamięci do śledzenia nowych castingów z bazy _galeriatwarzy.pl_.
- Śledzi najnowsze przesłuchania publiczne.
- Generuje unikalne identyfikatory i utrzymuje ich ciągłość na serwerze (bez duplikatów) przy pomocy mechanizmu `Store`.
- Automatycznie rozsyła powiadomienia Native Telegram do powiązanych użytkowników (np. na numery identyfikatorów Telegram).
- Zawiera dedykowaną obsługę i sensory tekstowe wyświetlające opisy.
- Posiada wbudowaną z poziomu serwisu HA (`galeria_twarzy.clear_memory`) funkcję resetowania bazy dla testów.

*(Kolejne integracje będą dodawane sukcesywnie...)*

---

## 🛠 Instalacja przez HACS

Z racji tego, że repozytorium nie znajduje się (jeszcze) w domyślnej bazie globalnego sklepu HACS, dodanie go jest bardzo proste:

1. Otwórz swój panel **Home Assistant**.
2. Z menu głównego wybierz **HACS**, a następnie **Integracje** (Integrations).
3. Kliknij ikonę **Trzech Kropek** w prawym górnym rogu ekranu i wybierz **Niestandardowe repozytoria** (Custom repositories).
4. Wpisz/wklej ten adres URL:
   `https://github.com/dbuczynski/hassio-integrations`
5. W polu "Kategoria" wybierz **Integracja** (Integration) i kliknij "Dodaj" (Add).
6. Repozytorium **dbuczynski Integrations** pojawi się na Twojej liście. Wystarczy w nie wejść, nacisnąć przycisk "Pobierz" / "Instaluj" i **uruchomić ponownie** instalację Home Assistant.

### Ważne po restarcie HA:
Pamiętaj, by po restarcie systemu finalnie aktywować te urządzenia przechodząc do:  
**Ustawienia** -> **Urządzenia oraz usługi** -> Przycisk **Dodaj Integrację** -> Wyszukaj np. _Galeria Twarzy_.
