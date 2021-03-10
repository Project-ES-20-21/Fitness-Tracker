# Algemene uitleg
We plaatsen accelerometer aan een kettlebell en deze zal dan gebruikt worden om de oefeningen te tracken. Ergens in de kamer zal een boek of poster voorzien worden met nummers op met daarbij een reeks van bijhorende oefeningen. Hieruit zullen de spelers kunnen afleiden welke serie van oefeningen ze moeten uitvoeren. Als de spelers een juiste oefening uitvoeren zal de batterij opgeladen worden en zal dit een stijging van het balkje op de display veroorzaken. Als het balkje voor de eerste keer helemaal vol is, zullen we een getal laten vrijgeven van het digitaal cijferslot. Als de spelers een incorrecte beweging uitvoeren zou het balkje niet mogen groeien. Als de spelers te dicht bij elkaar komen zal de broker een signaal uitsturen. We zullen dit dan straffen door ons batterij leeg te maken of te verminderen. Doorheen het spel zal er energie verbruikt worden en zal het balkje dus krimpen. Als de batterij helemaal leeg is, zou het onmogelijk moeten zijn zijn om andere opdrachten uit te voeren.

# Kanalen
## ESP32 op kettlebell
- Het kanaal "esp32/fitness/nmrOef" zal gebruikt worden om het nummer van de oefeningenreeks te publishen. 
- Het kanaal "esp32/fitness/OKmessage" wordt gebruikt om door te geven of de oefeningenreeks juist is of fout.
- Het kanaal "esp32/fitness/LCDmessage" geeft weer of er gemeten wordt en als de oefeningen juist of fout zijn.

## ESP32 met display
- Het kanaal "esp32/fitness/control" zal gebruikt worden om POWEROFF (3 zal dan gestuurd worden) en  POWERON (4 zal dan gestuurd worden). Dus als het cijfer drie gepublished wordt moeten alle andere proeven wachten totdat het cijfer 4 gepublished wordt.
- Het kanaal "esp32/fitness/cijferAlohomara" zal een nummer publishen van het cijferslot.

