# esphome-aqhh-automatic-pet-fountain

ESPHome component for AQHH's Automatic Pet Water Fountain (MY01)

[Manual](resources/AQHH-MY01-manual.pdf) - [ESPHome Official site](https://esphome.io/)

## TUYA datapoints

|DP ID|Function Point|Type|Description|
|---|---|---|---|
|1|Fountain power|switch| |
|2|Mode|enum|0 Continuous mode - 1 Intermittent mode|
|3|Filter replace reminder|int|Default 60 days|
|4|Clean reminder|int|Default 30 days|
|5|Filter reset|switch| |
|6|Clean reset|switch| |
|7|Filter replace reminder|int|Duplicated DP ID3|
|8|Clean reminder|int|Duplicated DP ID4|
|9| TBD |enum| |
|20| TBD |enum| |
|23|Error|bitmask| |
|101|LED light|switch| |
|102|Smart mode|switch| |
