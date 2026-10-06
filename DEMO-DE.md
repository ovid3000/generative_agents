# Smallville-Demo unter Windows

Die mitgelieferte Aufzeichnung zeigt Isabella Rodriguez, Maria Lopez und Klaus Mueller in der Pixelstadt. Sie benötigt keinen API-Schlüssel. Neue KI-Simulationen sind ein weiterer Einrichtungsschritt.

## Start

Voraussetzung: Python 3.12 und Git.

Beim Herunterladen mit Git lange Dateinamen aktivieren:

```powershell
git -c core.longpaths=true clone https://github.com/ovid3000/generative_agents.git
cd generative_agents
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements-demo.txt
cd environment/frontend_server
..\..\.venv\Scripts\python.exe manage.py migrate --noinput
..\..\.venv\Scripts\python.exe manage.py runserver 127.0.0.1:8000 --noreload
```

Im Browser öffnen:

http://127.0.0.1:8000/demo/July1_the_ville_isabella_maria_klaus-step-3-20/1/3/

Das Serverfenster geöffnet lassen. Mit den Pfeiltasten lässt sich die Karte erkunden. Die Oberfläche lädt Phaser, jQuery und Bootstrap aus dem Internet.

Die Demo-Weboberfläche wurde für Django 5.2 aktualisiert. Die ursprüngliche requirements.txt enthält ältere Forschungspakete; für die Demo ausschließlich requirements-demo.txt verwenden. Das Backend für neue KI-Entscheidungen ist noch nicht modernisiert.

Geprüft: Django-Systemprüfung ohne Fehler; Demo-Ansicht intern mit HTTP 200 erzeugt; alle 26 referenzierten lokalen Grafikdateien vorhanden; Bewegungsdaten der drei Figuren enthalten. Die Browserdarstellung wurde bisher nicht visuell bestätigt.

## Unser nächstes Experiment

Drei Figuren mit unterschiedlichen Persönlichkeiten sollen eine Teeparty organisieren. Vor dem ersten neuen KI-Lauf legen wir Modellzugriff und Kostenrahmen fest. API-Schlüssel bleiben außerhalb des Repositorys.
