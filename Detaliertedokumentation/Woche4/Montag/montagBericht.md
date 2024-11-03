# Wochenbericht Nr. 3  
**Zeitraum:** 21.10.2024  
**Firma:** DGI, Köln  
**Abteilung:** Netzwerk und Serveradministration  

---

## Tagesbericht: Traefik und Redlib im Docker-Umfeld

| Tag      | Ausgeführte Arbeiten | Einzelstunden | Gesamtstunden |
|----------|-----------------------|---------------|---------------|
| **Montag** | **Daily Meeting** <br> Gegenseitige Vorstellung und Austausch: "Was macht Team A und B?" um 10 Uhr | 10:00 - 10:30 | 0,5 Stunden |
|           | **Analyse und Implementierung von Traefik** <br> Intensive Auseinandersetzung mit Traefik als Reverse-Proxy und Aufbau eines Beispiel-Setups gemäß der offiziellen Traefik-Dokumentation: [Link zur Dokumentation](https://doc.traefik.io/traefik/user-guides/docker-compose/basic-example/) | 10:30 - 12:00 | 1,5 Stunden |
|           | **Aufsetzen der Traefik-Konfiguration** <br> Erstellung einer `docker-compose.yml`-Datei, die Traefik als zentralen Reverse-Proxy im Netzwerk verwendet, einschließlich der Konfiguration für Dashboard und HTTP-Zugriff: <br> - Aktivierung des `insecure API` Modus für das Dashboard zur Überwachung <br> - Einbindung des Docker-Sockets zur automatischen Erkennung neuer Container <br> - Bereitstellung eines HTTP-Einstiegspunkts auf Port 80 für Traefik | 12:00 - 13:30 | 1,5 Stunden |
|           | **Testen des Setups** <br> Start der Docker-Container und erfolgreicher Aufruf des Traefik-Dashboards unter `localhost:8081` zur Prüfung aktiver Verbindungen und Konfigurationen | 13:30 - 14:00 | 0,5 Stunden |
|           | **Mittagspause** | 14:00 - 14:30 | 0,5 Stunden |
|           | **Einrichtung und Integration von Redlib** <br> Integration von Redlib als zusätzlicher Service im Docker-Umfeld, inkl. Erstellen eines Docker-Images für Redlib basierend auf einer `Dockerfile`: <br> - Erstellung der Dockerfile und Konfiguration wie folgt: <br> ```dockerfile <br> FROM alpine:latest <br> COPY redlib /Users/jmann/Desktop/redlib-docker/redlib <br> RUN chmod +x /Users/jmann/Desktop/redlib-docker/redlib <br> ENTRYPOINT ["/Users/jmann/Desktop/redlib-docker/redlib"] <br> ``` | 14:30 - 16:30 | 2 Stunden |
|           | **Test und Validierung der Redlib-Integration** <br> Prüfung der Redlib-Integration in Docker und Verifizierung des korrekten Funktionierens innerhalb des Netzwerks | 16:30 - 17:00 | 0,5 Stunden |

**Gesamtstunden:** 8 Stunden

---
