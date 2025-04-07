
Miniprojekt for fiktivt firma "Solar". 


Forklaringer:


Bruker nedlastet CSV-filer om kunder, salg, retur, datoer, regioner og produkter.

Lager "hierarchy" for kolonene "Continent", "Country" og "Region"

Lager ny kolonne "Start of the Week" i Power Query der begynnelsen på hver uke er utskilt fra datoer i Solar_Calender table

Lager ny kolonne "Start of the Month" i Power Query der begynnelsen på hver måned er utskilt fra datoer i Solar_Calender table

Lager ny kolonne "Start of the Year" i Power Query der begynnelsen på hvert år er utskilt fra datoer i Solar_Calender table

Kobler "tables" sammen med "primary keys" med "one-to-many- relationships" i datamodellvisningen. 

Lager "measure": TotalQuantity som summerer alle tall fra OrderQuantity-kolonnen i Solar_Sales.

Lager "measure": QuantityReturned som summerer alle tall fra ReturnQuantity-kolonnen i Solar_Returns.

Lager ny kolonne  RetailPrice i Solar_Sales som henter "ProductPrice" fra "Solar_Product_Lookup" med "Related" - funksjonen.

Lager "measure": Revenue som ganger pris med antall varer i Solar_Sales table.

Lager "measure": Total Revenue som summerer alle tall fra Revenue-kolonnen i Solar_Sales.

Lager "measure": Total Cost som summerer alle tall fra Revenue-kolonnen i Solar_Sales og ganger med Productcost.

Lager "measure": Total Profit som bruker Total Revenue measure og trekker fra Total Cost measure.

Lager "measure": QuantityReturned som summerer alle tall ReturnQuantity i Solar_Returns.

Lager "measure": QuantitySold som summerer alle tall per rad fra OrderQuantity i Solar_Sales.

Lager "measure": Return Rate som deler QuantityReturned med QuantitySold med bruk av "Divide" - funksjonen.

Lager "measure": Total Returns som teller antall rader i Solar_Returns -table med "COUNTROWS" - funksjonen.

Lager "measure": Total Orders som teller antall unike rader i Solar_sales -table med "DISTINCTCOUNTROWS" - funksjonen.

Lager "Bar chart": Viser Total Orders sortert etter underkategorier.

Kopierer forrige "Bar chart": Viser Total Orders sortert etter hovedkategorier.

Lager "Matrix": Viser Total Orders of Return Rate etter produktnavn. Legger til "conditional formating".

Lager "Line chart": Viser profitt over tid.






















