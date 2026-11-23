# Klusjes-Oorlog v0.8.1-beta

Kleine update op basis van v0.8.0-beta.

- Klusjesbeheer: bewerkformulier opent direct onder aangeklikte klusjesrij.
- Na opslaan of annuleren sluit het inline formulier en blijft de lijst op dezelfde plek.
- Eén bewerkformulier tegelijk; opnieuw op Bewerken klikken klapt het dicht.
- Het formulier voor **Nieuw klusje** blijft onderaan beschikbaar.
- Geen wijziging aan Supabase, accounts, competitiegegevens of RPC-functies. Geen SQL-update.

## Installeren

Upload de websitebestanden uit de hoofdmap en de volledige map `avatars` naar je bestaande live GitHub-repository. Controleer vóór upload dat `SUPABASE_URL` verwijst naar het juiste project. De map `setup` bevat historische SQL-migraties die niet opnieuw hoeven te worden uitgevoerd.

## Test

Kies Admin Mode → Klusjesbeheer, zoek een klusje midden in de lijst en klik Bewerken. Controleer dat het formulier direct onder de rij opent, de invoer is overgenomen en de pagina niet naar de onderkant springt. Sla een wijziging op en controleer dat het formulier verdwijnt zonder de huidige zoekfilter te verliezen. Test ook Annuleren, een tweede rij openen en Nieuw klusje toevoegen.
