---
title: Aansluitvoorwaarden
layout: home
---

# Aansluitvoorwaarden en Ketentest LINDA Dataportaal

Deze pagina beschrijft de aansluitvoorwaarden voor het LINDA Dataportaal en de ketentesten voor de levering van sessiedata over openbare laadinfrastructuur. Dit document beschrijft de uit te voeren testen met als doel het aantonen dat aan de aansluitvoorwaarden en datakwaliteitseisen voor het LINDA Dataportaal wordt voldaan.  

Uitgangspunten zijn:
1.	Het LINDA Dataportaal en de supportoffice is operationeel.
2.	Koppelvlakken zijn operationeel.
3.	De testomgeving is beschikbaar 
4.	Rapportages met testresultaten zijn beschikbaar.

Gegevens die worden aangeleverd hebben betrekking op de locaties van laadpalen en de laadsessies. Getest zal worden of de aanlevering van data aan NDW plaatsvindt conform de OCPI 2.2.1 standaard, met specifiek de modules “Locations”  en “CDR”.

| Testvoorbereiding         | Gereed     | 
|--------------|-----------|
| Belangrijke voorwaarde voor het kunnen starten van de test is dat het LINDA endpoint op de Dexter staging omgeving bereikbaar is en dat Autorisatie is geregeld. | V      |
| Voorafgaand aan de test is er al een offline controle geweest van een OCPI-record (CDR en Location) om te valideren dat deze inhoudelijk correct is.      | V  |

# LINDA endpoints voor Dexter staging omgeving: 

Voor het aanleveren van OCPI 2.2.1 CDR: POST xxxxx
Voor het aanleveren van Locations: POST xxxx

De specificaties voor beide endpoints zijn gelijk, waarbij alleen de body andere input verwacht (CDR of Locations). 
 
Body: Xxx invullen door NDW
Autorisatie: aan te leveren door NDW

client_id : xxxx
client_secret: wordt verstrekt door NDW 
grant_type
gebruik de vaste waarde: client_credentials
scope
gebruik de vaste waarde: xxxx

Verbinding met het endpoint kan getest worden middels cURL:
curl xxxxx (aan te leveren door NDW)

# Test omschrijvingen

Er wordt vanuit gegaan dat de aan te leveren CDR en Locations voldoen aan xxxx. Indien niet aan de eisen wordt voldaan zal de ontvangende kant een errorcode 400 terug geven. Indien een CDR of Location succesvol is ontvangen, wordt er een http 202 naar leverancier gestuurd.

|   Happy flow   | | | | | |
|---|---|---|---|---|---|
| Testcase  | Actie leverancier  | MST versie  | Actie NDW  | Verwachte resultaat  |OK/NOK   |   
| Aanleveren MST met 1 locatie  |  Verifieert MST acceptatie van Dexter | 1  |  NDW verifieert dat xml bestand is ontvangen en geaccepteerd door Dexter | Verifieer Locatie in  Dexter.  | V  |
|  Aanleveren MST met meerdere locaties | Verifieert MST acceptatie van Dexter  | 2 | NDW verifieert dat xml bestand is ontvangen en geaccepteerd door Dexter. | Verifieer locaties in Dexter | V  |
|  Aanleveren MST na updaten van één locatie. | Verifieert MST acceptatie van Dexter.  | 3  | NDW verifieert dat xml bestand is ontvangen en geaccepteerd door Dexter.  |  Verifieer locaties in Dexter. | V |
| Aanleveren MDP voor 1 locatie met MST versie 3. | Verifieert MDP acceptatie van Dexter.  | 3  | NDW verifieert dat xml bestand is ontvangen en geaccepteerd door Dexter. | Verifieer data in Dexter. | V |
| Aanleveren MDP voor 1 locatie met MST versie 2.  | Verifieert MDP acceptatie van Dexter.  | 2 | NDW verifieert dat xml bestand is ontvangen en geaccepteerd door Dexter. | Verifieer data in Dexter.  | V |

|   Unhappy flow   | | | | | |
|---|---|---|---|---|---|
| Testcase  | Actie leverancier  | MST versie  | Actie NDW  | Verwachte resultaat  |OK/NOK   |   
| Aanleveren van MST met oude versie. |  Stuur het MST xml bestand naar Dexter. | 3  |  NDW verifieert dat xml bestand is ontvangen maar niet geaccepteerd door Dexter. | NDW stuurt een NACK (zie response codes)   | V  |
|  Aanleveren MDP met oude versie. | Stuur het MDP xml bestand naar Dexter.  | 2 | NDW verifieert dat xml bestand is ontvangen maar niet geaccepteerd door Dexter. | Verifieer locaties in Dexter | V  |
|  Aanleveren MST met ongeldige prefix. | Stuur het MST xml bestand naar Dexter.  | -  | NDW verifieert dat xml bestand is ontvangen maar niet geaccepteerd door Dexter. | NDW stuurt een NACK (zie response codes) | V |
| Aanleveren MDP met ongeldige locatie. | Stuur het MDP xml bestand naar Dexter.  | 3  | NDW verifieert dat xml bestand is ontvangen maar niet geaccepteerd door Dexter. | NDW stuurt een NACK (zie response codes) | V |

Indien nodig kunnen er nog additionele tests worden uitgevoerd.

# Responses (voor beide endpoints):
 
- 202: de aanlevering is succesvol verlopen.
- 400: de meegeleverde input bevat fouten. Afhankelijk van de soort fout (fout in XML definitie, fout in data, of fout in aangeleverde locaties) wordt er een foutcode en beschrijving meegegeven.
- 401: authenticatie fout, de token wordt niet geaccepteerd of is verlopen.
- 403: de gebruiker heeft geen rechten om de meegeleverde data aan te leveren. De authorisatie gebeurt op prefix-basis.
- 500: server fout.



