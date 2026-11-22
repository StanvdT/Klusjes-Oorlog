# Klusjes-Oorlog v0.8.0-beta

## Beta release
Dit pakket is gebaseerd op de geteste v0.7.18-alpha. Het bevat geen nieuwe spelregels, databasetabellen of Supabase-migraties. Alleen de actuele versie, beta-changelog, automatische updatecontrole (alpha én beta) en PWA-cache zijn bijgewerkt.

## Installatie op GitHub Pages LIVE
1. Maak zoals gebruikelijk een onafhankelijke databaseback-up.
2. Controleer in `index.html` dat `SUPABASE_URL` verwijst naar het bedoelde project. Het pakket gebruikt de bestaande **LIVE** URL `https://yhevmkrgstgdhbzcynmt.supabase.co` en bijbehorende publieke publishable key. Gebruik dit bestand niet ongewijzigd voor een testwebsite.
3. Upload de volgende items uit de **hoofdmap** naar de root van je live GitHub-repository: `index.html`, `sw.js`, `version.json`, `manifest.webmanifest`, `favicon.svg`, `icon-192.png`, `icon-512.png` en de hele map `avatars/`.
4. Commit, open de website en ververs met Ctrl+F5. Controleer `v0.8.0-beta` in de footer en onder Account → Instellingen.
5. Test aanmelden, competities, badges, Users en de zichtbaarheid van bestaande back-ups. Voer voor deze beta géén reset uit.

## SQL
**Geen SQL uitvoeren voor v0.8.0-beta.** De map `setup/` bevat uitsluitend SQL en leesmij-bestanden van eerdere versies als archief. De database moet al op de geteste v0.7.18-alpha staan.

## Publicatie en compatibiliteit
- De PWA service-worker gebruikt cache `klusjes-oorlog-v080-beta`.
- De updatecontrole accepteert nu zowel `-alpha` als `-beta`-versienummers.
- Bestaande gebruikersaccounts, scores, badges en Supabase-configuratie worden niet gewijzigd.
- De JavaScript-syntax en ZIP-integriteit zijn lokaal gecontroleerd. Dit is nog geen volledige browser- of live-acceptatietest.
