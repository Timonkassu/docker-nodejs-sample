# **Installation eines Projektes mit Markdown, Git, GitHub und Docker**

## **Installationsanleitung:**

1. **Fork auf GitHub erstellen**
    - Öffne das zu forkende Repositories über den Link: [docker-nodejs-sample](https://github.com/ICT-BLJ/docker-nodejs-sample)
    - Klicke im Repositories oben rechts auf den Button **Fork** und wähle im Menü den gewünschten Account aus.
    - Repositories in **Kommandozeile** klonen.

2. **Installation der notwendigen Pakete.**
    - NMP-Webseite anschauen für Erklärung der Pakete.
    - Falls noch nicht vorhanden **Nodejs** installieren.
    - Im Package.json können die Pakete angeschaut werden.

    ```json
    "dependencies": {
        "express": "^4.18.2",
        "pg": "^8.11.2",
        "sqlite3": "^5.1.2",
        "uuid": "^9.0.0",
        "wait-port": "^1.0.4"
    },
    ```

    - In der **Kommandozeile** eingeben, sodass die Pakete installiert werden.

    ```javascript
    npm install
    ```

3. **Docker konfigurieren und installieren**
    - Per Docker Webseite Docker Desktop installieren.
    - Wsl installieren und Neustart ausführen.
    - Um den Container zu konfigurieren muss ein Dockerfile erstellt werden. In diesem wird beschrieben wie der Container aufgebaut ist und welche Eigenschaften das Image haben sollte. Ausserdem wird darin definiert, welcher Befehl beim tarten ausgeführt wird.
    - Zusätzlich zum Dockerfile wird ein compose.yaml benötigt. Im YAML wird bestummen, wie die Applikation gestartet werden soll. Zusätzlich wird dort der Port festgelegt.
    - Das .dockerignore ist dazu gedacht, unnötige Datein beim Bauen des Images herauszufiltern.

4. **Starten der Applikation in einem Docker-Container**
    Das System kann durch das ausführen des Commands:

    ```javascript
    docker build -t docker-nodejs .
    ```

    gebaut und durch den Befehl im Dockerfile direkt gestartet werden.
