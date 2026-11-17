## Lokale Entwicklungsumgebung – biztrips-local

Da Frontend und Backend in getrennten Git-Repositories liegen, wurde ein zusätzliches Repository namens `biztrips-local` erstellt. Dieses enthält eine gemeinsame Docker-Compose-Konfiguration, welche das Frontend, Backend, die MariaDB-Datenbank und phpMyAdmin verwaltet.

Teammitglieder können die drei Repositories klonen und anschliessend das gesamte System über Docker Compose starten. Die benötigten Docker-Images werden dabei direkt anhand der Dockerfiles im Frontend- und Backend-Repository gebaut.

Vor dem Start muss eine lokale `.env`-Datei mit dem Datenbankpasswort erstellt werden. Anschliessend kann das gesamte System mit folgendem Befehl gestartet werden:

```bash
docker compose up --build -d
```

Dadurch werden alle Services automatisch gestartet und miteinander verbunden, ohne dass sie einzeln ausgeführt werden müssen.
