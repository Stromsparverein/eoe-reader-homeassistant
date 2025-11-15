# eoe-reader-homeassistant
Integration zum Auslesen des Energie-Österreich Readers in Homeassistant (https)


## How to use


### 1. API-Key am Reader Modul erstellen und Einträge in der Datei homeassistant-config-rest.yaml ersetzen.

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

#### Videoanleitung:

[![Watch the video](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/eoe-reader-screenshot.png)](https://raw.githubusercontent.com/Stromsparverein/eoe-reader-homeassistant/main/assets/eoe-reader-create-api-key-2025-11-15_11.44.29.mp4)



