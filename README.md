# eoe-reader-homeassistant
Integration zum Auslesen des Energie-Österreich Readers in Homeassistant (https)


## How to use


### 1. API-Key am Reader Modul erstellen und Einträge in der Datei homeassistant-config-rest.yaml ersetzen.


#### Videoanleitung:

[![Watch the video](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/eoe-reader-screenshot.png)](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/eoe-reader-create-api-key-2025-11-15_11.44.29.webp)

#### Zu ersetzende Einträge:

```html
<YOUR-READER-IP-HERE>  -> IP Adresse des Reader Muduls
<YOUR-READERS-TOKEN-HERE> -> API Key des Reader Moduls
```


```html
<!-- Beispiel -->
 <!-- original -->
  - resource: https://<YOUR-READER-IP-HERE>/api/v1/measurement
    scan_interval: 5
    headers:
      Authorization: "TOKEN <YOUR-READERS-TOKEN-HERE>"
    verify_ssl: false
    sensor:
 <!-- mit ersetzten Daten  -->
  - resource: https://192.168.178.174/api/v1/measurement
    scan_interval: 5
    headers:
      Authorization: "TOKEN ra3qvzp2u1dcs0mk34a3swt5dp0mf7cs"
    verify_ssl: false
    sensor:
```

### 2. Sensoren in Homeassistant Config integrieren

Inhalt von der angepassten homeassistant-config-rest.yaml kopieren und and das Ende der configuration.yaml von Homeassistant hinzufügen.

Üblicherweise ist diese Datei unter /config/homeassistant.yaml zu finden. (Dies kann allerdings je nach installationsmethode variiren)

### 3. Config überprüfen und Homeassistant neu starten

[![Watch the video](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/homeassistant-restart.png)](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/restart-homeassistant-2025-11-15_12.59.36.webp)


### 3. Sensoren in Energy-Dashboard einbinden

[![Watch the video](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/add-sensor-to-energydashboard.png)](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/add-reader-to-energyDashboard-2025-11-15_19.39.41.webp)

### 4. Sensoren in Homeassistant Custom-Dashboard einbinden

[![Watch the video](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/add-sensors-to-dashboard.png)](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/add-sensors-homeassistant-2025-11-15_19.44.55.webp)

![webp](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/add-sensors-homeassistant-2025-11-15_19.44.55.webp)