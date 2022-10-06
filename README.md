# e2-work-with-actions
In diesem Repository arbeiten wir mit Github Actions! <br> 
Hierbei handelt es sich um eine simple Java Spring Boot API. <br> 

### Folgende Tätigkeiten werden wir durchführen.
* Arbeiten mit Matrixen
* Arbeiten mit Caching
* Arbeiten Job Abhängigkeiten 
* Verwenden einer Github Action vom Marketplace
* Github Action via API Call triggern mit Postman
* Builden der Application
* Hochladen des Artefacts

Um mit den Übungen zu starten muss als erstes das Repository "geforkt" werden. <br>
Danach wird am eigenen Fork gearbeitet. 

## Übung 1: Arbeiten mit Matrixen
File: [Übung - Matrixen](.github/workflows/build-with-matrixen.yaml)
* öffne das File und löse sämtliche TODOS
- [ ] Füge das Event "push" hinzu, dass der Workflow bei jeder Repository Änderung startet
- [ ] Erweitere die Matrix um 1 Java Version und 1 OS (e.g. macos-latest)
- [ ] Starte den Workflow (die restlichen TODOs sind für Übung 5)

## Übung 2: Arbeiten mit Caching
File: [Übung - Caching](.github/workflows/caching.yml)
- [ ] TODOs open

## Übung 3: Arbeiten mit Job Abhängigkeiten
File: [Übung - Abhängigkeiten](.github/workflows/job-dependencies.yml)
- [ ] Es gibt 4 Jobs, dabei sind Job 2 und 4 von Job 1 abhänig - Erstelle diese Abhänigkeit
- [ ] Job 3 ist von Job 2 abhängig - Erstelle diese Abhängigkeit
- [ ] Starte den Workflow manuell über die Github UI

## Übung 4: Triggern eines Workflows via API (e.g. Postman)
- [ ] Füge bei einem Workflow das Event "workflow_dispatch" hinzu
- [ ] Erstelle einen API Key [Github PAT erstellen](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- [ ] Verwende Postman oder cUrl, um den Workflow zu starten
```bash
curl --request POST \
  --url https://api.github.com/repos/e2e-pipeline-workshop/e2-work-with-actions/dispatches \
  --header 'Authorization: Bearer >>> YOUR_TOKEN <<<' \
  --header 'Content-Type: application/json' \
  --data '{"event_type": "hello, I am a Postman Call"}'
  ```
  
  ## Übung 5: Builden der Applikation und Upload des Artefakts
  File: [Übung - Build](.github/workflows/build-with-matrixen.yaml)
- [ ] Suche im Marketplace nach der checkout Action
- [ ] Verwende die Action für die Java Installation
- [ ] Verwende einen Gradle Build
- [ ] Lade das Artefakt mit einer Aktion hoch