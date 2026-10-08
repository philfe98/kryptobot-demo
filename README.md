# Kryptobot – öffentliche Demo

Live-Seite: https://philfe98.github.io/kryptobot-demo/

## Funktionen
- Responsive Marktübersicht mit acht Binance-USDT-Spot-Paaren und 1h/4h/1d-Kerzen
- SVG-Kerzenchart, EMA 50 und EMA 200, Trendfilter
- Vereinfachter historischer EMA-Trendfolge-Backtest (nur Long, Gebühren 0,1 % je Transaktion, ohne Slippage)
- Lokales Paper-Trading mit **250 CHF** Startkapital und 0,1 % Gebühren

## Sicherheit und Einschränkungen
- **Keine echten Trades** und keine Binance-API-Schlüssel
- Keine Backend-Verbindung, keine Authentifizierung und kein Server-Speicher
- Paper-Portfolio wird ausschliesslich in `localStorage` dieses Browsers gespeichert. Es wird **nicht** zwischen Geräten synchronisiert.
- Kurse stammen von öffentlichen Binance-Endpunkten; die Simulation verwendet den letzten **abgeschlossenen** Kerzenschlusskurs, nicht den ausführbaren aktuellen Marktpreis.
- USD/CHF-Referenzkurs kommt von `open.er-api.com`; USDT wird für die CHF-Umrechnung näherungsweise wie USD behandelt. Wechselkurs, Gebühren, Spreads und reale Ausführung können abweichen.
- Positionen anderer Paare werden nur bewertet, wenn deren Kurs im aktuellen Browser geladen wurde. Bis dahin ist die Gesamtbewertung unvollständig.
- Der Backtest ist nur ein vereinfachter Vergleich auf dem geladenen Ausschnitt. Er berücksichtigt keine Slippage, Steuern, Finanzierung, Datenlücken oder Walk-forward-Validierung und ist **keine Renditeprognose**.

Der eigentliche Handelsbot wird separat im privaten Repository entwickelt. Dieses öffentliche Repository enthält nur eine eigenständige Demo-Oberfläche.
