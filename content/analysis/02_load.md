# Rapport kmom05 - utvärdera webbplatsers prestanda

Denna uppgiften handlar om att välja ut hemsidor och testa hur snabbt de laddas och om potentiella förbättringar inom laddningstid och användarbarhet.

## Urval
-----------------------
Samma som i kmom04.
- Sida A - https://www.avella.se/
- Sida B - https://www.robotevent.se/
- Sida C - https://apmproduction.se/

## Metod
-----------------------
För att samla in data och analysera prestanda kommer jag använda mig av följande verktyg:
 - Google PageSpeed Insights: Mäta mer komplexa prestandapoäng samt förslag på möjliga förbättringsområden.
 - DevTools inom Firefox(Network-fliken): För att mäta lokala laddningstider och resurser.
 - Google Sheets: För att dokumentera rådata och mätvärden. 

PageSpeed Insights förkortningar: <br>
 FCP (sekunder) - First Contentful Paint : Tiden det tar från användaren börjar ladda sidan tills den första synliga innehållsdelen visas ex bild <br>
 LCP (sekunder) - Largest Contentful Paint : Tiden det tar för den största synliga innehållsblocket att ladda ex bild, rubrik eller sektion <br>
 TBT (milisekunder) - Total Blocking Time : Den tid under sidladddningen som användaren inte kan interargera med sidan t ex på grund av Javascript som körs <br>
 CLS - Cumulative Layout Shift : Ett mått på hur mycket sidans layout skiftar under laddning <br>
 SI (sekunder) - Speed Index : Ett mått på hur snabbt sidans innehåll blir komplett visuellt under laddning <br>
 PS - Performance Score : Helhetsbetyg på flera mätvärden så som ovannämnda <br>
 AS - Accessibility Score : Hur tillgänglig sidan är för användare med funktionsnedsättningar <br>

Firefox Network Monitor förkortningar:
AR - Antal laddade resurser
ST (mb) - Storlek i MB
Tid (s) - Laddningstid i sekunder (Tiderna är ett snitt på 3st hårda omladdningar)

## Resultat
-----------------------
# Avella
[Länk till hemsidan](https://www.avella.se/) |
[Snapshot](https://imgur.com/a/I9HKnoJ) |
[A1(startsida)](https://www.avella.se/) |
[A2(About)](https://www.avella.se/copy-of-about-us) |
[A3(Products)](https://www.avella.se/copy-of-produkter) |
---
## PageSpeed Insights:
---
|  Dator   | Sida A1 | Sida A2 | Sida A3 | 
| :------: | :-----: | :-----: | :-----: | 
| FCP (s)  | 0.7     | 0.8     | 0.8     | 
| LCP (s)  | 3.2     | 2.8     | 0.9     | 
| TBT (ms) | 190     | 180     | 190     | 
| CLS      | 0       | 0       | 0       | 
| SI (s)   | 1.2     | 1.4     | 0.9     | 
| PS       | 76      | 78      | 93      | 
| AS       | 100     | 98      | 100     | 

|  Mobile   | Sida A1 | Sida A2 | Sida A3 |
| :------: | :-----: | :-----: | :-----: |
| FCP (s)  | 3       | 3.6     | 3       |
| LCP (s)  | 14      | 4.4     | 3.8     |
| TBT (ms) | 340     | 240     | 360     |
| CLS      | 0       | 0       | 0       |
| SI (s)   | 5.4     | 4.4     | 3.5     |
| PS       | 58      | 71      | 74      |
| AS       | 100     | 98      | 100     |

---
## Firefox Network Monitor
---
|         |  A1     |  A2     |  A3     |
| :-----: | :-----: | :-----: | :-----: |
| AR      | 143     | 163     | 151     |
| ST (MB) | 6.09    | 7.08    | 6.13    |
| Tid (s) | 4.23    | 5.17    | 4.48    |


# Robot Event
[Länk till hemsidan](https://www.robotevent.se/)
[Snapshot](https://imgur.com/Rg7g2Gt)
[B1(Startsida)](https://www.robotevent.se/)
[B2(Tjänster)](https://www.robotevent.se/17/2/vara-tjanster/)
[B3(Partners)](https://www.robotevent.se/17/4/partners/)
---
## PageSpeed Insights:
---
|  Dator   | Sida B1  | Sida B2 | Sida B3 | 
| :------: | :-----: | :-----: | :-----: | 
| FCP (s)  | 0.8     | 0.7     | 0.9     | 
| LCP (s)  | 1.3     | 1.4     | 1.2     | 
| TBT (ms) | 30      | 20      | 30      | 
| CLS      | 0.024   | 0.022   | 0.019   | 
| SI (s)   | 0.9     | 1.2     | 1       | 
| PS       | 96      | 95      | 96      | 
| AS       | 95      | 100     | 97      |

|  Mobile  | Sida B1  | Sida B2 | Sida B3 | 
| :------: | :-----: | :-----: | :-----: | 
| FCP (s)  | 3.5     | 4       | 4.8     | 
| LCP (s)  | 8.5     | 10.2    | 8.3     | 
| TBT (ms) | 70      | 100     | 160     | 
| CLS      | 0       | 0       | 0.018   | 
| SI (s)   | 5.6     | 6.1     | 5.8     | 
| PS       | 64      | 61      | 60      | 
| AS       | 95      | 100     | 97      |

---
## Firefox Network Monitor
---

|         |  B1     |  B2     |  B3     |
| :-----: | :-----: | :-----: | :-----: |
| AR      | 76      | 51      | 33      |
| ST (MB) | 2.19    | 3       | 1,7     |
| Tid (s) | 1,07    | 0,657   | 0,565   |

# APM Production
[Länk till hemsidan](https://apmproduction.se/)
[Snapshot](https://imgur.com/LoJXHmi)
[C1(Startsida)](https://apmproduction.se/)
[C2(Flöde)](https://apmproduction.se/flode/)
[C3(Kontakt)](https://apmproduction.se/kontakt/)
---
## PageSpeed Insights:
---
|  Dator   | Sida C1 | Sida C2 | Sida C3 | 
| :------: | :-----: | :-----: | :-----: | 
| FCP (s)  | 0.7     | 0.7     | 0.7     | 
| LCP (s)  | 1.1     | 1       | 1.2     | 
| TBT (ms) | 40      | 0       | 0       | 
| CLS      | 0.018   | 0       | 0       | 
| SI (s)   | 1.2     | 0.9     | 0.8     | 
| PS       | 97      | 98      | 97      | 
| AS       | 90      | 89      | 85      |

|  Mobile  | Sida C1 | Sida C2 | Sida C3 | 
| :------: | :-----: | :-----: | :-----: | 
| FCP (s)  | 2.7     | 2.6     | 2.6     | 
| LCP (s)  | 5.3     | 5       | 5       | 
| TBT (ms) | 60      | 0       | 0       | 
| CLS      | 0       | 0       | 0       | 
| SI (s)   | 3.4     | 2.6     | 2.6     | 
| PS       | 75      | 78      | 78      | 
| AS       | 87      | 86      | 82      | 

---
## Firefox Network Monitor
---

|         |  C1     |  C2     |  C3     |
| :-----: | :-----: | :-----: | :-----: |
| AR      | 56      | 23      | 25      |
| ST (MB) | 3,04    | 1,15    | 1,2     |
| Tid (s) | 1,06    | 0,754   | 0,665   |

## Analys
-----------------------
Vi börjar med en analys på Avella.
FCP (First Contentful Paint): På desktop är FCP bra på alla sidor, den är snabb med mätvärden under 1 sekund vilket jag anser är ett bra betyg och laddar snabbt. Detta innebär att användaren ser första delen av innehållet snabbt och får sidan att kännas snabb.
LCP (Largest Contentful Paint): LCP på startsidan och about sidan är något långsammare än vad jag skulle föredra och kan förbättras för att uppnå en snabbare upplevelse. Dock väldigt bra tid på produkt sidan. Men på mobil sidan är det mycket långsamt och användaren får vänta hela 14 sekunder för att huvudinnehållet ska laddas. 
TBT (Total Blocking Time): Jämfört med dom andra sidorna ligger Avella efter i TBT, genom att förbättra detta får användaren en snabbare och mer responsiv användarupplevelse, ett högre TBT innebär fördröjningar i sidans interaktivitet.
PS (Performance): Här ligger Avella också efter de andra vilket indikterar att där finns utrymme för förbättringar, exempelvis då som nämndes innan att optimera bilder, minska laddningstider m.m vilket var det vi kom fram till genom resultaten ovan.

Robot Event:
FCP - På desktop är FCP mycket bra och konsekvent för alla sidor, användaren ser innehållet snabbt vilket ger en positiv upplevesle. På mobil är FCP betydligt långsammare och jag skulle säga att det är lite över rekommenderad tid för att användaren ska tycka att sidan är långsam. Förbättring här handlar om att minska laddningstider för de initiala resurser som visas.
LCP - Utmärkt på desktop vilket tyder på att stora element laddar snabbt. Däremot på mobil är det betydligt långsammare vilket visar att mobila användare stöter på stora fördröjningar innan de största innehållsblocket visas, för att lösa detta behövs de optimeras.
TBT - Skulle säga att det är grymt bra TBT med mycket låga värden. Detta visar att sidorna är mycket responsiva, fast de är lite högre på mobil skulle jag fortfarande säga att det är acceptabelt.
Performance - Mycket starkt på desktop men dras ner på mobil pga LCP. Generellt så är det mycket bra på desktop och majoriteten av förbättringarna kommer ligga på mobilsidan. För att vara en sån interaktiv hemsida är detta ett väldigt bra betyg skulle jag säga.

APM:
FCP - är mycket bra på desktop med tider på 0.7s för alla sidor. Detta gör precis som nämnt innan att användaren snabbt ser första innehållet på sidan och upplever sidan som snabb. Även fast den är något långsammare på mobil skulle jag säga att den är godkänd då generellt sätt alla sidor är långsammare på mobil. 
LCP - På desktop är LCP utmärkt, med tider mellan 1,0-1,2 sekunder för alla sidor. På mobil är det något långsammare och det finns förbättringspotential.
TBT - Här fick jag 0 ms på flera olika sidor, vet inte riktigt om det är korrekt eller inte men jag upplever sidan som väldigt snabb.
Performance - På desktop får APM väldigt bra betyg, jag tror att det grundar sig i att dom har en enkel hemsida utan mycket interaktiva grejer vilket gör hemsidan snabb.

## Referenser
[Avella](https://www.avella.se/) <br>
[Robot Event](https://www.robotevent.se/) <br>
[APM](https://apmproduction.se/) <br>
[Pagespeed](https://pagespeed.web.dev/) <br>
[Metrics](https://web.dev/explore/metrics) <br>
[GoogleDocs](https://docs.google.com/spreadsheets/d/e/2PACX-1vSkcxNuxQFcvmUEeRAKRlwtmBVCkmJX2iKX2DP2VhYVDTNbOtUNQRLbgHUc_w8FWFSKOwkme6K0gE4h/pubhtml) <br>

## Övrigt
-----------------------

Jobbat själv