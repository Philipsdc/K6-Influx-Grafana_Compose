## Docker - Grafana & InfluxDB

Il test è eseguito su docker. Di conseguenza tutte le procedure di inizailizzazione, installazione, esecuzione e visualizzazione presuppongono lo svolgimento su container docker. 

1. Installare [Docker Desktop](https://www.docker.com/products/docker-desktop/)
2. Aprire il terminale e posizionarsi sulla cartella
3. Inviare il comando
>```
>docker-compose up -d
>```
4. Ora i container saranno pronti per essere utilizzati. Aprire cmd e una volta installato [k6](https://k6.io/docs/get-started/installation/) inviare il seguente comando dalla cartella samples:
>```
>k6 run --duration 60s --out influxdb=http://localhost:8085/myk6db prova.js
>```
5. Aprire il browser in questa [pagina](http://localhost:3000/) e autenticarsi come Admin inserendo sia nel campo username che nel campo password:***admin***