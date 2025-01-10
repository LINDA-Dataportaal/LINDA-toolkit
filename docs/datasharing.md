---
title: Data sharing
layout: home
nav_order: 2
---

# Dataprocessen binnen het LINDA Dataportaal

Een belangrijk onderdeel van de LINDA Toolkit zijn de afspraken over het aanleveren, verzamelen, ontsluiten en gebruiken van data. Die afspraken staan hieronder.

# Datalevering
  
1. Het beschikbaar stellen van sessiegegevens van openbare laadpalen aan NDW vindt uitsluitend plaats na een schriftelijke opdracht van de data-eigenaar. Als het data-eigenaarschap bij de contract-/concessiehouder ligt, dan geeft die toestemming aan betreffende CPO. Ligt het data-eigenaarschap bij een CPO, dan geeft deze rechtstreeks toestemming aan NDW voor het toevoegen van sessiegegevens van openbare laadpalen aan het LINDA Dataportaal. 
2. Voor het vastleggen van de instemming wordt gebruik gemaakt van een standaard bevestigingsbrief tussen data-eigenaar en CPO, indien dat niet al in het contract is geregeld. De NAL-regio’s verzorgen deze standaard bevestigingsbrief en informeren alle gemeenten.
3. De instemming van de data-eigenaar aan een CPO, geeft een CPO toestemming om sessiegegevens van openbare laadpalen beschikbaar te stellen aan het LINDA-dataplatform bij NDW.
4. Een CPO stelt sessiedata van openbare laadpalen beschikbaar via de OCPI-standaard aan NDW. Specifiek gaat het voor het LINDA Dataportaal om toepassing van de Sessions module (CPO interface) en Locations module van de OCPI-standaard. Er wordt gebruik gemaakt van de meest recente, stabiele versie van OCPI, zoals beschreven op: https://github.com/ocpi/ocpi. 
5. Om de beheerlasten laag te houden en de controles op de datakwaliteit te kunnen automatiseren, worden de sessiegegevens van alle openbare laadpalen van een CPO via één connectie/bron en één autorisatiesleutel aangeboden aan en uitgewisseld met NDW conform het LINDA OCPI Profiel zoals beschreven in bijlage 2. 
6. NDW haalt de locatiegegevens van openbare laadpalen één keer per dag en de sessiegegevens elke twee weken op bij een CPO, conform het NL-OCPI-LINDA-profiel. 
7. De kosten het realiseren van de OCPI-koppeling door een CPO met het LINDA Dataportaal, zijn voor rekening van de CPO. Aan het verzamelen, opslaan en ontsluiten van data op het LINDA Dataportaal door NDW zijn geen kosten verbonden voor CPO’s.

# Datakwaliteit
8. De verantwoordelijkheid voor de kwaliteit van de sessie- en locatiegegevens van openbare laadpalen ligt bij een CPO. Het uitgangspunt is “beheer bij de bron”. De eisen die aan de data-uitwisseling en datakwaliteit gesteld worden zijn beschreven in bijlage 2 (het LINDA-profiel van de OCPI-standaard). Deze eisen worden met alle betrokkenen jaarlijks geëvalueerd en zo nodig aangepast als bijvoorbeeld wet- en regelgeving of beleidsontwikkelingen dat vereisen. Voor aanpassingen bij een CPO die niet zijn afgedekt door contractuele afspraken, is vooraf schriftelijke overeenstemming nodig tussen betrokken partijen.
9. Een CPO zorgt dat gegevens die uitgewisseld worden via de Sessions-module van OCPI (een CDR-record) de velden bevat, zoals beschreven in het LINDA-profiel van de OCPI-standaard.
10. Een CPO is verantwoordelijk voor het vastleggen van de daadwerkelijke, exacte locatie c.q. coördinaten van een openbare laadpaal, conform het betreffende verkeersbesluit en/of de verleende vergunning. Locatiegegevens worden aangeleverd aan het LINDA Dataportaal via de Locations-module van de OCPI-standaard.
11. Een CPO zal een melding over een onjuiste locatie c.q. onjuiste coördinaten van een openbare laadpaal, na verificatie van de melding, binnen 5 werkdagen dagen doorvoeren in haar eigen (bron)systeem. Meldingen over onjuiste locaties en coördinaten worden ingediend bij en verzameld door de supportdesk van NDW en via een standaard bericht teruggekoppeld aan CPO’s.
12. NDW controleert of de sessie- en locatiegegevens van openbare laadpalen die door een CPO worden aangeleverd, voldoen aan de kwaliteitseisen, zoals omschreven in bijlage 2. Alleen data die voldoen aan die eisen worden opgenomen in het LINDA-dataportaal.
13. Indien NDW constateert dat de data van een CPO niet voldoen aan de eisen en richtlijnen zoals geformuleerd in bijlage 2, dan informeert NDW de betreffende CPO en de NAL-regio’s per omgaande over de geconstateerde gebreken. De CDR-records die gebreken bevatten worden niet opgenomen in het LINDA Dataportaal. De betreffende CPO zal uiterlijk binnen 4 weken de gecorrigeerde CDR-data opnieuw aanleveren aan NDW. Via de NAL-regio’s worden de contracthouder(s)- en/of concessiegever(s) geïnformeerd zodat zij, indien nodig, in overleg kunnen treden met de betreffende CPO over de datalevering en datakwaliteit.    
14. NDW levert na elke import van CDR-gegevens van een CPO online inzicht aan geautoriseerde gebruikers van betreffende CPO en contracthouders en/of concessiegevers over de datakwaliteit en de mate waarin de CPO voldoet aan de eisen, zoals geformuleerd in bijlage 2.

# Dataverzameling
15. NDW is de technisch en functioneel beheerder van het LINDA-dataportaal en de onderliggende infrastructuur. Aan het beheer ligt een Dossier Afspraken en Procedures (DAP) ten grondslag tussen NDW en de NAL-regio’s.
16. NDW heeft passende technische en organisatorische maatregelen genomen om de geleverde gegevens te beveiligen en te beschermen tegen ongeoorloofd of onrechtmatig gebruik, onopzettelijk verlies, vernietiging of beschadiging. NDW werkt volgens de algemeen erkende Baseline Informatiebeveiliging Overheid (BIO) beveiligingsnorm van de Rijksoverheid conform NEN-ISO/IEC 27001 en NEN-ISO/IEC 27002
17. NDW bewaart de historische laadpaaldata voor een periode van 10 jaar. 

# Data-ontsluiting
18. Data-eigenaren krijgen via het LINDA Dataportaal inzicht en toegang tot hun eigen gegevens.
19. Data van het LINDA Dataportaal worden in twee vormen beschikbaar gesteld: KPI-data of CDR-data.
20. KPI-data zijn geaggregeerde data die betrekking hebben op één van de mogelijke KPI’s zoals genoemd in bijlage 4. Beschikbare KPI-data worden door NDW kosteloos beschikbaar gesteld aan geautoriseerde gebruikers via een exportmogelijkheid in haar Dexter-portaal of via een API. Toevoeging van nieuwe KPI’s loopt via de NAL-regio’s en gebeurt alleen als er middelen voor ontwikkeling en beheer van nieuwe KPI’s beschikbaar zijn. 
21. CDR-data zijn gegevens van individuele laadsessies, conform de OCPI-standaard en het LINDA OCPI Profiel, zoals weergegeven in bijlage 2. CDR-data worden door NDW uitsluitend beschikbaar gesteld aan geautoriseerde gebruikers via een REST API en in overeenstemming met de procedure voor een data-aanvraag zoals beschreven in bijlage 4.
22. Bij CDR data kunnen individuele velden uitgesloten worden van data delen, als op basis van een data-aanvraag (zie bijlage 4) beoordeeld wordt dat betreffend veld niet gedeeld kan/mag worden met de aanvrager of niet past binnen doel van de aanvraag.
23. Data die via een API beschikbaar worden gesteld, vereisen altijd een sleutel (API-key). Deze sleutel/ (API-key) is gekoppeld is aan de aanvrager van de data (data-gebruiker) en onderdeel van de Verwerkersovereenkomst. Deze info wordt gebruikt voor monitoring van het gebruik.

# Datagebruik
24. Iedereen kan een aanvraag indienen voor toegang tot de data, via de aanvraagprocedure zoals beschreven in bijlage 5. Dit betekent niet dat iedereen ook daadwerkelijk toegang krijgt tot de data. Elke aanvraag moet onderbouwd worden en wordt beoordeeld door het LINDA Datateam. Alleen indien aan de voorwaarden wordt voldaan, wordt een aanvraag gehonoreerd.
25. Elke data-aanvraag wordt geregistreerd in een register en is openbaar toegankelijk. 
26. Bij een positieve beoordeling ontvangt de aanvrager een gebruikersovereenkomst waarin de afspraken zijn vastgelegd. In bijlage 6 is een concept gebruikersovereenkomst beschreven.
27. Na ondertekening van de gebruikersovereenkomst door de data-aanvrager (datagebruiker), krijgt NDW van het LINDA Datateam de opdracht om de data beschikbaar te stellen aan de datagebruiker onder de voorwaarden zoals beschreven in de gebruikersovereenkomst.
28. NDW monitort per datagebruiker het gebruik van de data op o.a. het aantal API-requests en downloads, en rapporteert hierover per maand aan het LINDA Datateam. Deze metrics kunnen in de toekomst uitgebreid worden om beter inzicht te krijgen in de performance, het gebruik en de effectiviteit van de API’s en downloadmogelijkheden.
29. Indien geconstateerd wordt dat data oneigenlijk gebruikt worden of sprake is van een datalek, dan neemt NDW passende maatregelen, zoals het afsluiten van de data-gebruiker of het doen van een melding bij de Autoriteit Persoonsgegevens. Ook vindt terugkoppeling plaats aan de CPO’s zodat zij, indien nodig, aan hun wettelijke verplichtingen kunnen voldoen.
30. Vooralsnog zijn de data alleen voor geautoriseerde gebruikers toegankelijk. Alle partijen streven ernaar om data die geen privacygevoelige gegevens bevatten, als open data beschikbaar te stellen, dat wil zeggen zonder beperkingen aan (her)gebruik. Pas na schriftelijke instemming van de data-eigenaar, worden data als open data beschikbaar gesteld.
