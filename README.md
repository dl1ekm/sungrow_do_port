# sungrow-do-port
## Beschreibung
Diese Dateien stellen eine Ergänzung zur Sungrow SHxxRT HomeAssistant Intragion von mkaiser (https://github.com/mkaiser/Sungrow-SHx-Inverter-Modbus-Home-Assistant) dar.

Es wurden mit Hilfe von Informationen aus dem Photovoltaik-Forum (https://www.photovoltaikforum.com/thread/166134-daten-lesen-vom-sungrow-wechselrichtern-modbus) die wichtigsten Register zur Steuerung des DO-Ports (potentialfreier Kontakt) des Wechselrichters ergänzt.

Dabei habe ich mich auf die Einstellungsmöglichkeiten der Betriebsart **Regelmodus Last** konzentriert.

*Disclainer: Diese Implementierung ist sicher verbesserungswürdig und stellt meinen ersten Versuch dar, den Sungrow-Wechselrichter DO-Port mit HA zu steuern. Es gibt sicher schönere Wege und besseren Code ;-). Diese Dateien sollen explizit nur als Anregung dienen. Ich übernehme natürlich keinerlei Garantie oder Verantwortung - ihr wisst selber, was ihr tut.*

## Anleitung zur Installation

* Die Datei **sungrow_do.yaml** wird in das Verzeichnis ``integrations`` kopiert, so wo auch die Datei ``modbus_sungrow.yaml``von mkaier liegt
* Der Inhalt der Date **modbus_sungrow_sensors.yaml** beschreibt die zusätzlichen Sensoren. Dieer Text wird am besten ganz am Anfang hinter ``-sensors``in die originale Datei ``modbus_sungrow.yaml kopiert, da wo auch die anderen Sensosren definiert werden.
* In der Datei **dashboard_do.yaml** habe ich den Export eines Test-Dashboards hinterlegt. Darin wird das Verhalten des on-board Webinterface nachgebildet, d.h. es werden nur die Parameter sichtbar gemacht, welche auch in der jeweiligen Einstellung sinnvoll sind. Diesen Code einfach in ein neues Dashboard kopieren im Homeassistant (Raw-Konfigurationseditor)


