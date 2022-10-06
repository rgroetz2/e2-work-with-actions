# e2-work-with-actions
In diesem Repository arbeiten wir mit Github Actions! <br> 
Hierbei handelt es sich um eine simple Java Spring Boot API. <br> 

### Folgende T�tigkeiten werden wir durchf�hren.
* Arbeiten mit Matrixen
* Arbeiten mit Caching
* Arbeiten Job Abh�ngigkeiten 
* Verwenden einer Github Action vom Marketplace
* Github Action via API Call triggern mit Postman
* Builden der Application
* Hochladen des Artefacts

Um mit den �bungen zu starten muss als erstes das Repository "geforkt" werden. <br>
Danach wird am eigenen Fork gearbeitet. 

## �bung 1: Arbeiten mit Matrixen
File: [�bung - Matrixen](.github/workflows/build-with-matrixen.yaml)
* �ffne das File und l�se s�mtliche TODOS
- [ ] F�ge das Event "push" hinzu, dass der Workflow bei jeder Repository �nderung startet
- [ ] Erweitere die Matrix um 1 Java Version und 1 OS (e.g. macos-latest)
- [ ] Starte den Workflow (die restlichen TODOs sind f�r �bung 5)

## �bung 2: Arbeiten mit Caching
File: [�bung - Caching](.github/workflows/caching.yml)
- [ ] TODOs open

## �bung 3: Arbeiten mit Job Abh�ngigkeiten
File: [�bung - Abh�ngigkeiten](.github/workflows/job-dependencies.yml)
- [ ] Es gibt 4 Jobs, dabei sind Job 2 und 4 von Job 1 abh�nig - Erstelle diese Abh�nigkeit
- [ ] Job 3 ist von Job 2 abh�ngig - Erstelle diese Abh�ngigkeit
- [ ] Starte den Workflow manuell �ber die Github UI

## �bung 4: Triggern eines Workflows via API (e.g. Postman)
- [ ] F�ge bei einem Workflow das Event "workflow_dispatch" hinzu
- [ ] Erstelle einen API Key [Github PAT erstellen](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- [ ] Verwende Postman oder cUrl, um den Workflow zu starten
```bash
curl --request POST \
  --url https://api.github.com/repos/e2e-pipeline-workshop/e2-work-with-actions/dispatches \
  --header 'Authorization: Bearer >>> YOUR_TOKEN <<<' \
  --header 'Content-Type: application/json' \
  --data '{"event_type": "hello, I am a Postman Call"}'
  ```
  
  ## �bung 5: Builden der Applikation und Upload des Artefakts
  File: [�bung - Build](.github/workflows/build-with-matrixen.yaml)
- [ ] Suche im Marketplace nach der checkout Action
- [ ] Verwende die Action f�r die Java Installation
- [ ] Verwende einen Gradle Build
- [ ] Lade das Artefakt mit einer Aktion hoch