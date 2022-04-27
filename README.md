 # Performance audit van Science 
Bij web performance  draait alles om het snel maken van websites, inclusief het snel laten lijken van langzame processen. Laadt de site snel, kan de gebruiker er snel mee aan de slag en geeft hij geruststellende feedback als iets even duurt om te laden (bijvoorbeeld een laad spinner)? Zijn scrollen en animaties soepel?
 ![Screenshot (11)](https://user-images.githubusercontent.com/90189815/165076416-2ca6f8c6-f71d-455e-ad99-21513a48faed.png)



## ContentAudit
Website: https://www.science.org/

Datum:26-4-2022
![Screenshot (12)](https://user-images.githubusercontent.com/90189815/165272658-5f9e7650-3b71-401c-9975-d36810d5fdf5.png)

### First Contentful Paint (FCP)
De performance van websitr Science score 0,8s op Desktop. Er zijn een paar verbeter punten waarmee de scores omhoog  kunnen krijgen.
##### Reducing overall font load time:
Er zijn groot bestanden  fonts die duurt even  om te laden . daardoor de FCP entje traag. Deze kunnen worden opgelost door:

*  Gebruik font display bijvoorbeeld:
 
      @font-face { font-family: Helvetica; font-display: swap; }

* Wacht met het gebruik van aangepaste lettertypen totdat ze zijn geladen
##### Serve images in next-gen formats
performance  kijkende die site gebruik images formats jpg dat maak de lading traag Deze kunnen worden opgelost door bijvoorbeeld Afbeeldingsformaten zoals WebP en AVIF bieden vaak betere compressie dan PNG of JPEG, wat snellere downloads en minder gegevensverbruik betekent dus kunnen gebruik andere format


### Time to Interactive (TTI)
##### Om TTI sinelgeid te verbeteren kan Science paar dingen doen:
* onnodig javascript verwijderen

* Splits de JavaScript-bundel om alleen de code te verzenden die nodig is voor de initiële route wanneer de gebruiker een applicatie laadt.
### Speed Index
Terwijl alles wat je doet om de laadsnelheid van de pagina te verbeteren, uw snelheidsindex zal verbeteren..Bovendien zijn er een paar specific verbeter punten waarmee ze de scores omhoog kunnen krijgen zoals :
 * Reduce javascript execution time.
 * Minify and compress your code
### Total Blocking Time (TBT)
TBT meet de totale tijd dat een pagina niet reageert op gebruikersinvoer, zoals muisklikken, schermtikken of toetsenborddrukken.
Je kunt de score's omhoog krijgen door:
* Verwijder al het gebruik van document.write() in code.
* verwijder long-time tasks. er zijn vier long tasks gevonden
### Largest Contentful Paint (LCP)
Hier een element gevonden, het is groot img , om de score  omhoog kunnen krijgen hier moeten kies het juiste image formaat

### Cumulative Layout Shift (CLS)
De elments (main.content, div.card-content, div.ExternalAdMedium__wrapper.py-4, ul.list-inline.comma-separated, i.list-inline-item). de issue hier gebruiken elementen zonder afmetingen.Ze zouden beter kunnen afmeting geven.

## Bronnen

## Licentie

![GNU GPL V3](https://www.gnu.org/graphics/gplv3-127x51.png)

This work is licensed under [GNU GPLv3](./LICENSE).
