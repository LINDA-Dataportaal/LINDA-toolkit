---
title: NL-OCPI-LINDA Profiel
layout: home
---

# Inleiding

Het LINDA Dataportaal volgt de OCPI-standaard om de (her)bruikbaarheid van data te waarborgen. Om een consistente en uniforme manier van aanlevering van laaddata en laadlocaties te realiseren, is een set richtlijnen (het OCPI LINDA-profiel) ontwikkeld in samenwerking met het Nationaal Kennisplatform Laadinfrastructuur (NKL). Het doel is om een uniform profiel te bieden voor de aanlevering van Charge Detail Records (CDR's) middels het Open Charge Point Interface (OCPI)-protocol door Charge Point Operators (CPO's) die laadpalen in de publieke ruimte plaatsen en exploiteren.

Het OCPI LINDA-proefiel is opgesteld in het kader van de landelijke samenwerking tussen gemeenten, samenwerkingsregio's, CPO's en het NDW voor het aanleveren van data voor het LINDA-dataportaal. Dit dataportaal verzamelt gegevens en stelt die beschikbaar voor de monitoring en planning van laadinfrastructuur. Door het harmoniseren van de aanlevering van deze gegevens via het OCPI-protocol, wordt beoogd de efficiëntie en betrouwbaarheid van de laadinfrastructuur in Nederland te verbeteren. Belanghebbenden binnen de laadinfrastructuursector, waaronder de NAL-regio's, CPO's, EV-Roaming Foundation en de NAL werkgroep Open Protocollen, Data en Markten, zijn betrokken bij het opstellen van deze richtlijnen in het OCPI LINDA-profiel.

Het OCPI LINDA-profiel is geen aanpassing van de OCPI-standaard zelf, maar het beschrijft richtlijnen voor het gebruik van de standaard. De OCPI-standaard kan gezien worden als het “wat” en het OCPI LINDA-profiel als het “hoe”. Het OCPI LINDA-profiel biedt verduidelijkingen, aanvullende eisen en richtlijnen die niet expliciet in het generieke OCPI-protocol zijn opgenomen, maar die essentieel zijn voor de uniformiteit en betrouwbaarheid van de data-aanlevering aan het LINDA Dataportaal. Door het OCPI LINDA-profiel te volgen, wordt uiteindelijk gewaarborgd dat de data uniform wordt aangeleverd aan het NDW vanuit CPO's, waarbij het OCPI-protocol als basis dient voor de gegevensuitwisseling.

# Doelstelling NL-OCPI-LINDA-profiel

De doelstellingen die beoogd worden met het OCPI LINDA-profiel zijn:
1. Harmonisatie van datalevering door de wijze waarop CPO’s sessie- en locatiegegevens via het OCPI-protocol aanleveren aan het NDW te standaardiseren.
2. Verbetering van datakwaliteit door heldere specificaties voor de kwaliteit van de aangeleverde data, inclusief accuraatheid, actualiteit, compleetheid, precisie en consistentie.
3. Eenduidige implementatie van OCPI door het verduidelijken van de toepassing van het OCPI-protocol binnen de Nederlandse markt.
4. Efficiënte overdracht van laadstations door procedures voor de overdracht van laadstations tussen CPO’s, inclusief het behoud van historische data en de consistente koppeling van nieuwe en oude laadpunt-ID’s.

# Datakwaliteitseisen
Voor alle velden binnen de CDR-objecten uit de OCPI-specificatie gelden de volgende eisen aan datakwaliteit:
1. Accuraat: De data die worden aangeleverd, zijn een correcte weergave van de werkelijkheid op dat moment.
2. Actueel: De data hebben een ouderdom die past bij het beoogde gebruik. 
3. Compleet: De vereiste datapunten zijn aanwezig, alle velden worden geleverd zoals gespecificeerd in de standaard en deze handreiking, en bevatten de data van alle laadpunten in beheer op het moment van meten.
4. Precies: De data bevatten de mate van detail passend bij het gebruik en conform de specificaties in dit document en de OCPI-standaard.

# OCPI LINDA-profiel

Voor een compleet beeld van (het gebruik van) de openbare laadinfrastructuur moet binnen de OCPI-standaard een aantal velden verplicht meegestuurd worden. Het NL-OCPI-LINDA-profiel specificeert aanvullende richtlijnen voor deze velden om ervoor te zorgen dat alle laadpalen consistent en volledig (kunnen) worden gemonitord.

Onderstaande tabellen bevatten zowel verduidelijkingen als aangescherpte richtlijnen die voortvloeien uit het OCPI LINDA-profiel. De aanvullende omschrijvingen en specificaties zijn van toepassing op de implementatie van de "CDR module" en de "Locations module" binnen de meest recente OCPI-versies (2.1.1 en 2.2.1). De tabellen geven een overzicht van de officiële specificaties, inclusief verduidelijkingen en aangescherpte verplichtingen die specifiek gelden volgens het LINDA OCPI Profiel.

## CDR en Locations module OCPI 2.1.1

|   OCPI 2.1.1 veld (referentie hoofdstuk)|Omschrijving |Specificatie kwaliteitsnorm |Specificatie formaat|Verplicht|Motivatie|
|---|---|---|---|---|---|
| tariffs (hfd. 10.3.1)|  Tarief-object met informatie over tarief CDR | -  |  - | Ja  | Om effectief de contractuele afspraken te monitoren en transparantie te bieden aan de EV-rijder is deze data nodig. |
|  total_parking_time (hfd. 10.3.1)| -  |-|Ja | Totale duur laadsessie zonder dat er energie is geladen |
| evses (hfd. 8.3.1 en 8.3.2) |EVSE-object met informatie over laadstations op deze locatie| -  |- | Ja| Door hergebruik van de “location module” in de specificatie is dit in versie 2.1.1 |
| location : evses : evse_id (hfd. 8.3.2) | -  | - | -| Ja | Om laadlocaties te kunnen monitoren op gebruik is het laadpunt essentieel.|
| operator (hfd. 8.3.1 en 8.4.2) | CPO informatie | - | - | Ja| Consolidatie wordt vergemakkelijkt met deze informatie. |
