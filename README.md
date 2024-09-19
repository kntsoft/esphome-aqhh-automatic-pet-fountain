# esphome-aqhh-automatic-pet-fountain

ESPHome component for AQHH's Automatic Pet Water Fountain (MY01)

[Manual](resources/AQHH-MY01-manual.pdf) - [ESPHome Official site](https://esphome.io/)

## TUYA datapoints

|DP ID|Function Point|Type|Description|
|---|---|---|---|
|1|Fountain power|switch| |
|2|Mode|enum|<ol start="0"><li>Continuous mode</li><li>Intermittent mode</li><ol>|
|3|Filter replace reminder|int|Default 60 days|
|4|Clean reminder|int|Default 30 days|
|5|Filter reset|switch| |
|6|Clean reset|switch| |
|7|Filter replace reminder|int|Duplicated DP ID3|
|8|Clean reminder|int|Duplicated DP ID4|
|9|Water status|enum|<ol><li>No water</li><li>Water</li><ol>|
|20| TBD |enum| |
|23|Error|bitmask|<ul><li>00000000 No error</li><li>0X000001 No water</li><li>0X000001 Generic error</li></ul>|
|101|LED light|switch| |
|102|Smart mode|switch| |

## Errors behaviour

Generic error, status led red

```log
21:44:52 [D] [tuya:372] Datapoint 23 update to 0X000020
````

No water, status led red blinking

```log
21:47:04 [D] [tuya:355] Datapoint 9 update to 1
21:47:04 [D] [tuya:372] Datapoint 23 update to 0X000001
```

No error, status led white

```log
21:48:01 [D] [tuya:355] Datapoint 9 update to 2
21:48:01 [D] [tuya:372] Datapoint 23 update to 00000000
```
