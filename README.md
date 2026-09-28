# 🪙 Bitcoin Price Tracker

Ett objektorienterat Python-skript som hämtar realtidsdata för Bitcoin-priset via CoinGecko REST API, validerar datan, samlar in historik över tid och sparar mätningarna till strukturerade JSON- och CSV-filer.

## 🚀 Funktioner & Nyckelkoncept
* **Objektorienterad programmering (OOP):** Använder en basklass (`BaseTracker`) och en underklass (`BitcoinTracker`) med arv och `super().__init__()`.
* **API-anrop & Externa bibliotek:** Hämtar levande marknadsdata via `requests` API-anrop.
* **Felhantering & Validering:** Skyddat mot nätverksfel med `try/except` och `raise_for_status()`, samt validerar att mottagna priser är giltiga.
* **Automation & Loopar:** Samlar in flera mätningar automatiskt i en `for`-loop med pausintervall (`time.sleep`).
* **Filhantering:** Exporterar automatiskt klistan till både **JSON** och **CSV**.

## 🛠️ Installation & Användning

1. **Klona projektet:**
   ```bash
   git clone <https://github.com/Shorka84/Bitcoin_tracker.git>
   cd bitcoin-tracker

Installera beroenden: pip install requests

Kör programmet: python main.py


📊 Datastruktur & GDPR-efterlevnad
Projektet genererar två filer med insamlad historik:
bitcoin_data.json: Innehåller fullstäniga mätningar tillsammans med GDPR-metadata som verifierar att endast offentlig marknadsdata utan personuppgifter (PII) behandlas.
bitcoin_data.csv: En platt tabellstruktur med kolumnrubriker redo att öppnas i kalkylprogram som Excel.
