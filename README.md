# Domáca Meteostanica (PWA)

Progresívna webová aplikácia (PWA) pre premenu starého tabletu alebo mobilu na permanentnú meteostanicu a domáci panel. Optimalizované pre zobrazenie na šírku (landscape) s vysokou čitateľnosťou.

## 🚀 Hlavné Funkcie

- **Veľké Digitálne Hodiny:** Žlté vysoko čitateľné hodiny inšpirované segmentovými domácimi stanicami s lokálnym slovenským formátom dátumu.
- **Globálna Predpoveď počasia:** Integrácia na bezplatné Open-Meteo API (nevyžaduje API kľúč).
- **Inteligentná Lokalizácia:** - Automatické vyhľadávanie miest po celom svete pomocou zabudovaného našepkávača (Geocoding API).
  - Možnosť zamerania presnej polohy cez GPS (`navigator.geolocation`).
- **PWA (Progressive Web App):** Možnosť inštalácie priamo na domovskú obrazovku zariadenia, pričom beží v režime **fullscreen** bez ovládacích prvkov prehliadača.
- **Trvalé úložisko (Persistence):** Posledná vybraná poloha sa ukladá do `localStorage`, takže po reštarte zariadenia sa automaticky načíta správne mesto.

## 🛠️ Nasadenie na Cloudflare Pages

1. Vytvorte nové repozitár na vašom GitHub účte a nahrajte doňho obsah tohto ZIP archívu.
2. Prihláste sa do **Cloudflare Dashboardu**.
3. Prejdite do **Workers & Pages** -> **Create application** -> **Pages** -> **Connect to Git**.
4. Vyberte vaše repozitár (`meteo.ensecnet.net` alebo akýkoľvek názov).
5. V konfigurácii buildu nastavte *Framework preset* na **None** a všetko ostatné nechajte predvolené.
6. Kliknite na **Save and Deploy**.

### 🔗 Priradenie vlastnej subdomény (`meteo.ensecnet.net`)
1. V detaile projektu v Cloudflare Pages prejdite na záložku **Custom domains**.
2. Kliknite na **Set up a custom domain**.
3. Zadajte vašu subdoménu `meteo.ensecnet.net`.
4. Ak doménu spravujete priamo v Cloudflare, DNS CNAME záznam a SSL certifikát sa nakonfigurujú kompletne automaticky.

## 📁 Štruktúra projektu

- `index.html` - Hlavný aplikačný kód (HTML5, CSS3 Grid, Vanilla JS).
- `manifest.json` - PWA manifest pre integráciu do operačného systému mobilu/tabletu.
- `_headers` - Cloudflare konfiguračný súbor pre vypnutie agresívnej cache nad manifestom, aby sa aplikácia korektne aktualizovala.
- `README.md` - Táto dokumentácia.
