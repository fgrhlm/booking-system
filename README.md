## Projekt 1 - Stugmäklaren
### Webbtjänster och molnteknologi 21

# TLDR; FOR ENGLISH READERS
This is a mvp of an booking system implemented in NodeJS
The project was part of an assignment in the course "Web-services and cloud-technology"

## Allmänt
Försöker följa dessa: 
    - https://expressjs.com/en/advanced/best-practice-performance.html
    - https://expressjs.com/en/advanced/best-practice-security.html
    - https://github.com/goldbergyoni/nodebestpractices
    - https://sodocumentation.net/node-js/topic/10785/route-controller-service-structure-for-expressjs

Eftersom det uppmuntrades starkt att inte blanda gammal JS och modern ES så har jag valt att
aktivera ECMAScript moduler: 

```line 6: package.json: "type":"module"```

Detta tillåter mig att använda snäppet modernare import syntax istället för require

## Kör projektet

### Production
Prodcontainern är helt "statisk". Alltså inga volymer som mountas osv.

```
docker-compose --profile prod up -d
```

### Dev
I devcontainern mountas ``` app/ ``` som en volym.
Måste installera paket lokalt för att detta skall funka eftersom ingen npm install körs i containern.
```
docker-compose --profile dev up -d
```