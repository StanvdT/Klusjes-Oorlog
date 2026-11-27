# Klusjes-Oorlog v0.8.3-beta

Nieuwe interface voor klusjes in een competitie: categorieën, compacte regels met beschikbaarheid en vorige uitvoering, uitklapbare details inclusief onderhoudsfrequentie, de bestaande bevestigingsknop, sorteren en filter Nooit uitgevoerd.

**Geen SQL-migratie.** De database, puntenberekening, wachttijden, onderhoudsfrequenties, badges, beheerfuncties en reset/herstel blijven ongemoeid.

Installeer de zeven websitebestanden en de map `avatars/` in de GitHub Pages hoofdmap. Controleer eerst de Supabase URL/key in `index.html` en test bij voorkeur op het testproject.

Bij periodieke klusjes toont de laatste uitvoerdatum de gedeelde onderhoudshistorie van het duo, ook uit eerdere matches. Bij niet-periodieke klusjes wordt de laatste uitvoering binnen de huidige match getoond.

De JavaScript-syntax en ZIP-integriteit zijn lokaal gecontroleerd. Browsergedrag met echte accounts moet nog worden getest.
