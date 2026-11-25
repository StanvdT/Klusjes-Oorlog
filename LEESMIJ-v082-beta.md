# Klusjes-Oorlog v0.8.2-beta — onderhoud zonder blokkade

## Nieuw
- Alle geselecteerde klusjes zijn meteen uitvoerbaar, ook als de onderhoudsfrequentie nog niet verstreken is.
- `Gepland` is een informatief overzicht van aankomend onderhoud. Dezelfde klusjes staan tevens onder `Alles` en `Beschikbaar` (tenzij de persoonlijke wachttijd loopt).
- De gedeelde onderhoudstermijn start bij de eerste match met dat klusje, of opnieuw bij de laatste uitvoering door een van beide spelers.
- Na de deadline verschijnt de klus onder `🔥 Tijd om aan te pakken!`. Pas bij achterstand begint de puntenbonus te groeien, tot maximaal ×2.
- De bestaande persoonlijke wachttijd en eindtijd van de competitie blijven daadwerkelijke blokkades.

## Installatie — éérst op TEST
1. Maak een onafhankelijke Supabase-back-up. Gebruik uitsluitend de database van je testproject.
2. Voer `setup/supabase_v082_frequentie_zonder_blokkade.sql` uit in Supabase SQL Editor. Dit verandert geen spelgegevens. De reset-/herstelfunctie wordt uit voorzorg uitgeschakeld wegens schemafingerprintwijziging.
3. Upload de websitebestanden uit de hoofdmap, plus `avatars/`, naar de TEST GitHub Pages-repository. Controleer dat `SUPABASE_URL` en `SUPABASE_KEY` in `index.html` naar de juiste omgeving verwijzen. In het ZIP staat de bestaande LIVE-verbinding, dus wijzig beide waarden voordat je de TEST-site publiceert.
4. Test met een nieuwe competitie: een nog nooit uitgevoerd klusje met een lange frequentie moet direct claimbaar zijn; `Gepland` toont wel de aftelklok. Voltooien moet de gewone punten geven en de gedeelde frequentieteller verversen. Test dat persoonlijke wachttijd en verlopen competitie blijven blokkeren en dat bonus pas na de deadline stijgt.
5. Controleer reset/herstel met een volledig compatibele nieuwe momentopname op TEST; voer PAS daarna `setup/supabase_v082_systeembeheer_opnieuw_goedkeuren.sql` uit om Systeembeheer opnieuw vrij te geven. Een reset op LIVE is niet nodig.
6. Herhaal na geslaagde tests de SQL-migratie op LIVE, controleer functies en upload daarna de websitebestanden naar LIVE; controleer live URL en key expliciet. Herkeur de resetconfiguratie op LIVE pas als alle controles zijn geslaagd.

## Let op
- De bestaande `klusjes_eerste_beschikbaarheid` en uitvoeringshistorie blijven bewaard; geen reset van ritmes, punten of achievements.
- Vorige privé-snapshots zijn niet automatisch compatibel met de nieuwe schemahandtekening; bewaar onafhankelijke back-ups buiten Supabase.
- Dit is een SQL-update én website-update. Alleen de website uploaden kan nog steeds tot serverfouten leiden.
