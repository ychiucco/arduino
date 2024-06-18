- `ard config init`
```
Config file written to: /Users/yuri/Library/Arduino15/arduino-cli.yaml
```

- `cat /Users/yuri/Library/Arduino15/arduino-cli.yaml`
```
board_manager:
    additional_urls: []
```

- `ard sketch new MyFirstSketch`
```
Sketch created in: /Users/yuri/Desktop/GitHub/arduino/MyFirstSketch
```

- `ard core update-index`
```
Sto scaricando l'indice: package_index.tar.bz2 scaricato
```

- `ard board list`
```
Porta                           Protocollo Tipo              Nome scheda FQBN            Core
/dev/cu.BLTH                    serial     Serial Port       Sconosciuto
/dev/cu.Bluetooth-Incoming-Port serial     Serial Port       Sconosciuto
/dev/cu.YT18                    serial     Serial Port       Sconosciuto
/dev/cu.usbmodem14132401        serial     Serial Port (USB) Arduino Uno arduino:avr:uno arduino:avr
```

- `ard core install arduino:avr`
```
...
La piattaforma arduino:avr@1.8.6 è installata
```

- `ard core list`
```
ID          Installato Ultimo Nome
arduino:avr 1.8.6      1.8.6  Arduino AVR Boards
```

- `ard compile --fqbn arduino:avr:uno MyFirstSketch`
```
Lo sketch usa 924 byte (2%) dello spazio disponibile per i programmi. Il massimo è 32256 byte.
Le variabili globali usano 9 byte (0%) di memoria dinamica, lasciando altri 2039 byte liberi per le variabili locali. Il massimo è 2048 byte.

Piattaforma utilizzata Versione Percorso
arduino:avr            1.8.6    /Users/yuri/Library/Arduino15/packages/arduino/hardware/avr/1.8.6
```

- `ard upload -p /dev/cu.usbmodem14132401 --fqbn arduino:avr:uno MyFirstSketch`
```
Nuova porta di caricamento: /dev/cu.usbmodem14132401 (serial)
```
