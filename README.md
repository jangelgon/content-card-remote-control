# Remote Control card #

<img src="https://github.com/dimagoltsman/ha-custom-lovelace-cards/blob/master/remote-control/screenshot.png?raw=true" height="400">

# This repo is now migrated to: https://github.com/dimagoltsman/generic-remote-control-card #


Put js and the folder files in your www dir and add the js files to your resources in ui-lovelace.yaml
```
resources:
  - url: /local/content-card-remote-control.js
    type: js
```

if it doesnt load, copy ```content-card-remote-control``` dir to ```www```

configuration is very easy. first, find your broadlink id for sending packets (can be found under HA services page),
and then just configure the broadlink codes for each button.

All buttons are configured according to the id of the button in the html section of `remote-html.js`

simple remote example:
```
  - type: "custom:content-card-remote-control"
    broadlink_host: '192.168.1.151'
    name: Hisense
    remote_template: simple
    buttons:
      power:
      source: "JgBYAAABKpITEhQQFRAVEBMSFBEUERMREzYWNBQ1FTQVNRQ1FRAVNRQREzYUEBUQFTUUERQRFBAVNRQRFDUVNBUREzYTNhQ2EwAFTgABKUcVAAxWAAEpRxQADQU="
      button1:  
      button2:  
      button3:  
      button4:  
      button5:  
      button6:  
      button7:  
      button8:  
      button9:  
      buttonClear:
      button0:
      buttonEnter:
      exit:
      info:
      menu:
      left: "JgBQAAABKpIVEBMRFRAVEBUQFBEUERQREjcUNhM2EzYUNhM2FBAVNRQ1FRAVEBQ2EzYTERYPFRAVERM2EjcUEBUREzYUNRQ2FAAFTQABKUgUAA0FAAAAAAAAAAA="
      right: "JgBQAAABKZIUERQRExIUERMRFBEVEBQREzYVNBU1FDUUNRU1FBETNhUQFBEUERQ1FTQVERMSExEUNRU1FDUUERUQFDUUNhM2FAAFTgABKEgVAA0FAAAAAAAAAAA="
      top: "JgBQAAABKJIVERQRExIVDxQRFBEUERQREzYTNhU1FTQWMxU1FBETNhQRFDUUNRUQFTUUERMSFBAUNRURExIUNRQQFTUUNRM2FQAFTgABKEgVAA0FAAAAAAAAAAA="
      bottom: "JgBQAAABKZIUERMSEhIUERUQFBEUERMSEzYUNhM2FTQUNhM2FBAUNhQ1FTQVNRQRFDUUERUQExITEhQRFBAVNBURFDUVNBU1FAAFTQABKUgVAA0FAAAAAAAAAAA="
      ok: "JgBUAAkACXEAASiTFRAUERQRFBETEhQRExEUERU1FDUUNRU1FDUUNRYPEzcTNhQQFjQTEhU0Fg8UERQRFBEVNBQRFDYSEhQ1FTQVNRQABU4AASlIFAANBQAAAAA="
      back:
      volplus: "JgCgAJSSEg8QEBIPERAPMhEyDxERDxAxEDESLxAyEREPEREQEBAQlBARDxIQEBAREi8PMhEvEhAQMRExDzIREBARDhISDhAyEBEQEQ8REi8RAAdclJMRDxAREREPEREwEi8SEBARDzIQMhAwDzESEBARERAQEBKSEg8QEBAREREPMREyDjESDhIwETESLxEQEBEREBAQETAPERERERAQMRAADQUAAAAAAAAAAA=="
      volmin: "JgDgAJGUERAREA8RERERLxAyEBEQEBAyDjMRLxMwEBEOEg8RERAOlBMPEBEQEBEQEg8REBAQETIQMBEyEDAQEBIvEjEQMBIPDxIPEhEPETASAAdclJMSDhAREBEPEw8xEi8QERARDzEPMxEwETEQEBEREBASDhGTEg8RDxASEBEOERAQERARMBIwEi8RMhAQETEOMhExEBAREBARDxIPMhEAB1yWkRAQERAQERAREDESLxEREBARMBAxEDERMBEQEREOExAQEZIQERAQEhAQEQ0TEBEQEBExEDEQMBIwERARAA0FAAAAAAAAAAA="
      mute: "JgCgAJaSEQ8RDxIPEg8SMBIvEg8SDxIvETERMBAxEg8SDxIPEQ8SkhIPEg8SDxIPETASDxIPERARLxIwEi8SDxIPEjARMBIwERASDREQEjASAAdhlJMSDxEQERARDxIvEjASDxEPETESMBEwEjARDxAQEg8SDxKSEg8REBEPEg8SMBEQEQ8REBIwEi8SLxIPEg8SLxIwEi8SDxEQEg8RMBEADQUAAAAAAAAAAA=="

```


LG remote example:
```
      - type: "custom:content-card-remote-control"
        broadlink_host: '192.168.1.151'
        name: LG Tv
        remote_template: simple
        buttons:
          power: "JgBYAAABKpIVEBURFDUWEBQRFBETEhURFDUVNRUQFTUVNRQ2FDUTNxQTExEUEhE3ExQTERMSFRITNRU1FDYUEhI3FDUVNRM3FQAFMwABKEoWAAxMAAEqSBUADQU="
          source: "JgBYAAABJpMSExEUETgRFBEUERMSExITEjcSOBETEjgROBI4ETgSOBETEjgROBITEhMSEhM3ETgTNxITERMSOBE4EjgRExITEQAFGwABJkoSAAxGAAElSxIADQU="
          button1:  
          button2:  
          button3:  
          button4:  
          button5:  
          button6:  
          button7:  
          button8:  
          button9:  
          buttonClear:
          button0:
          buttonEnter:
          exit:
          info:
          menu:
          channeldown:
          channelup:
          netflix:
          left: "JgBQAAABKpIVEBMRFRAVEBUQFBEUERQREjcUNhM2EzYUNhM2FBAVNRQ1FRAVEBQ2EzYTERYPFRAVERM2EjcUEBUREzYUNRQ2FAAFTQABKUgUAA0FAAAAAAAAAAA="
          right: "JgBQAAABKZIUERQRExIUERMRFBEVEBQREzYVNBU1FDUUNRU1FBETNhUQFBEUERQ1FTQVERMSExEUNRU1FDUUERUQFDUUNhM2FAAFTgABKEgVAA0FAAAAAAAAAAA="
          top: "JgBQAAABKJIVERQRExIVDxQRFBEUERQREzYTNhU1FTQWMxU1FBETNhQRFDUUNRUQFTUUERMSFBAUNRURExIUNRQQFTUUNRM2FQAFTgABKEgVAA0FAAAAAAAAAAA="
          bottom: "JgBQAAABKZIUERMSEhIUERUQFBEUERMSEzYUNhM2FTQUNhM2FBAUNhQ1FTQVNRQRFDUUERUQExITEhQRFBAVNBURFDUVNBU1FAAFTQABKUgVAA0FAAAAAAAAAAA="
          ok: "JgBUAAkACXEAASiTFRAUERQRFBETEhQRExEUERU1FDUUNRU1FDUUNRYPEzcTNhQQFjQTEhU0Fg8UERQRFBEVNBQRFDYSEhQ1FTQVNRQABU4AASlIFAANBQAAAAA="
          back:
          volplus: "JgBQAAABJZMTEhITETgSExEUERMSExITETgSOBITETgSNxM3ETgSOBEUETgRFBETEhMSExEUERMTNxISEzcROBM3ETgSOBI3EwAFGQABJkoSAA0FAAAAAAAAAAA="
          volmin: "JgBYAAABJpMSExEUETgSExEUERMSExEUETgSOBMREjgROBI4ETgSNxI4EjgRExITERQRExITEhMRFBETEjgROBI4ETgSOBE4EQAFGwABJkoSAAxFAAEmShIADQU="
          mute: "JgCgAJaSEQ8RDxIPEg8SMBIvEg8SDxIvETERMBAxEg8SDxIPEQ8SkhIPEg8SDxIPETASDxIPERARLxIwEi8SDxIPEjARMBIwERASDREQEjASAAdhlJMSDxEQERARDxIvEjASDxEPETESMBEwEjARDxAQEg8SDxKSEg8REBEPEg8SMBEQEQ8REBIwEi8SLxIPEg8SLxIwEi8SDxEQEg8RMBEADQUAAAAAAAAAAA=="
      
```


Mibox Remote example, thanx to Avi Abeksis! (code also from mibox):

<img src="https://github.com/dimagoltsman/ha-custom-lovelace-cards/blob/master/remote-control/content-card-remote-control/mibox/remote-back.png?raw=true" height="400">

```
- type: "custom:content-card-remote-control"
  broadlink_host: '192.168.1.151'
  name: Mibox
  remote_template: mibox
  buttons:
    top: "JgBOACITFSQWERYaFiQVEhUSFRsWGxQmFC8VAAGaJBEVJRQTFBwVJRQTFREWGxUbFSUULxQAAZ0iERYkFBMVGxYkFRIUExUbFRwVJRUvFAANBQAAAAAAAAAAAAA="
    bottom: "JgBOACMSFSUVEhUbFSYUEhUSFRwUJRQmFRIUAAGvIxEUJhUSFBwUJhUSFRIUHBUlFCYUExUAAa0jEhQlFRIWGxUkFhEWERYaFSUVJRUSFQANBQAAAAAAAAAAAAA="
    clickleft: "JgBOACMSFCYUExUbFCYVEhQSFSUVLhYbFRsWAAGaIxEVJRUSFhoVJRUSFRIVJRQvFRsVHBQAAZwjERUlFhAWGxYkFRIVERUmFC8VGxUcEwANBQAAAAAAAAAAAAA="
    clickright: "JgBOACMSFiQVERUdFCUUExUSFC8VEhUSFSUUAAGuJBEUJhMUEx0UJhUSFBMULxUSFRIVJBUAAa8iEhUkFRIWGxUkFhEWERUuFhEVEhUlFAANBQAAAAAAAAAAAAA="
    ok: "JgBOACISFyMVEhQcFiQVEhUSFS8UHBUSFS8VAAGaIhMUJhQSFRwTJxQTFREWLhQcFRITMBUAAZsiEhUlFBMTHRUlFRIVEhQvFRsWERUuFwANBQAAAAAAAAAAAAA="
    back: "JgBoACMRFiQUExQcFiQVEhYRFRsVLhUlFRwVAAGbIhIVJRURFhsVJRQTFRIWGhUvFCYUHBUAAZokERUlFRIUHBUlFBMUEhUcFC8VJRUbFQABmyMRFSUVEhQcFiQVEhUSFRsWLRUlFhsUAA0F"
    exit: "JgBOACMSFSUVEhUbFSUVEhYQFhsVLhUmEx0VAAGbIhEVJRUSFB0VJRQTFBMUHBQvFSUVGxYAAZojEhMmFRIVHBQlFRIVEhUbFDAVJRcZFAANBQAAAAAAAAAAAAA="
    info: "JgBoACMSEycUEhUcFCUWERYRFRwVJBUlFRIWAAGtIxEVJRUSFRsVJRUSFRIUHBQmFSUUExUAAa4hExUlFRIVGxQmFBMTFBMdFCYUJhQTFAABriMSEycUEhQdEycVERQTFRwVJBYkFhEVAA0F"
    home: "JgCCACMSFCYUExMdFSUVEhURFSUWEhMcFiQVAAGuIhIWJBUSFRsWJBUSFRIVJhMSFhwUJRUAAa4hFBQlFxAWGxQlFBMUExQmFRIUHBQmFQABrSQRFCYUExQcFCYUExQTFCUWERUcFSQWAAGuIxAWJBYRFRwVJBYRFRIWJBQTFRwTJxQADQUAAAAAAAA="
    power: "JgBOACMSFRIVLhUvFRIULxUSFC8VEhQvFi4UAAFiJBETFBMwFS4VEhUvFREWLhUSFS4VLhYAAWEjEhURFS8ULxUSFS4VEhUuFRIVLxUuFQANBQAAAAAAAAAAAAA="
    volumeup: "JgBOACQQFSUVEhUbFSUVEhUSFS4VJhQTFBMUAAGuIhIVJRUSFRwTJhUSFRIVLhQmFBMTFBUAAa0jEhUlFRIUHBUlFBMUExQvFSUVEhURFQANBQAAAAAAAAAAAAA="
    volumedown: "JgBOACMRFSUVEhQcFSUVEhUSFS4VLhUSFRwVAAGbIhIVJBYRFRwUJRYRFRIWLhUvFBIVHBQAAZskERQmFBMUHBYkFRIUEhUvFC8VEhQcFQANBQAAAAAAAAAAAAA="
```

PartnerTV Remote example, thanx to @VirtualL :

<img src="https://github.com/dimagoltsman/ha-custom-lovelace-cards/blob/master/remote-control/content-card-remote-control/partner/remote-screen-shot.png?raw=true" height="400">

```
- type: "custom:content-card-remote-control"
  broadlink_host: '192.168.1.151'
  name: PartnerTV
  remote_template: partner
  buttons:
    power: JgBQAAABJ5QWDxYPFTUVDxYPFRAVEBUPFjQVNBYPFjQVNBY0EzcVNBUQFRAVDxY0FRAVDxYPFg8VNRU0FTUVDxY0FTQWNBU1FQAFIgABJ0oWAA0FAAAAAAAAAAA=   #myLGTV
    volplus: JgBQAAABJ5QUERMSEzcTERQRExITEhMRFDYTNxMREzcTNhQ2EzcTNhMSEzYUERMSExITEhMRFBETNxMSEzYTNxM2EzcTNhM3EwAFJAABJ0sTAA0FAAAAAAAAAAA= #myLGTV
    volmin: JgBQAAABJ5QUEBYPFTUVEBUPFg8VEBUQFDUVNRUQFTQVNRU0FTUVNBU1FTQWDxURFBAVDxYPFRAVEBUPFjQVNRU0FTUVNBY0FQAFIgABJ0oWAA0FAAAAAAAAAAA=  #myLGTV
    partner: JgBQAAABKZMSExM3FBISOBM3ExITNxQ2FBITEhMTExITExMSEzcUNhM3FBITEhM3EzcTExMSEzcUEhM3EzcTEhMTEzcTNxMSFAAFNQABKUgUAA0FAAAAAAAAAAA=
    mute: JgBQAAABJ5QTEhQSEjYUERUQFBEUERQRFDUUNRUQFDYUNRU1FDUTNxU1FBAWDxU1FQ8WDxYPFRAVEBU0FTUVEBU0FTUVNBY0FQAFIgABJ0oWAA0FAAAAAAAAAAA=    #myLGtv
    record: JgBQAAABKJQTEhM3ExMTNxM3ExITOBM3ExITEhMTExITExMSEzcTNxM3EzgSOBMSExMSExMSExMUERQSExITNxM3EzcTOBM3EgAFNwABKEgTAA0FAAAAAAAAAAA=
    source: JgBYAAABJ5QTEhMSEzYVEBQRFBEUEBUQFDYUNRQRFDYUNRQ2FTQVNRU0FjQVEBQzFxAVEBUQFQ8WDxUQFDUWEBI3FTQWNBU0FQAFIwABJ0sUAAxSAAEnSxMADQU=  #myLGTV
    one: JgBQAAABKJMUEhM3ExITNxM3FBITNxM3ExITExMSFBITEhQSEzcTNxQ2ExITExQRFDYTExMSExMTEhQ2EzcTNxMTEzcUNhQ2FAAFNQABKEgTAA0FAAAAAAAAAAA=
    two: JgBQAAABKJMUEhM3FBETOBI4ExIUNhQ2FBITEhQSEhMTExMSEzcTNxQSEjgTEhMTEjgSExQSEhMTNxMTEjcUNxITEzcTNxM3EwAFNgABKEkTAA0FAAAAAAAAAAA=
    three: JgBQAAABKJMUEhM3ExITOBI4ExITNxM3FBITEhMTEhMTEhMTEzcTNxM3FDYUEhITEzcTExITExMTEhMSEzcTOBITEzcTNxM3EwAFNgABKEkTAA0FAAAAAAAAAAA=
    four: JgBQAAABKZIUEhM3ExIUNhQ2FBIUNhQ2ExIUEhQRFBITEhMTEzcTNxQRExMTNxQRFDYUEhQRFBITNxQ2ExIUNhQSEzcUNhQ2EwAFNgABKkcUAA0FAAAAAAAAAAA=
    five: JgBQAAABKJMTExM3ExITNxM3ExMTNxM3ExIUEhMSFBITEhQSEzcTNxQ2ExITNxMTFDYUERQSExITExM3ExIUNhQSEzcTNxQ2FAAFNQABKEkSAA0FAAAAAAAAAAA=
    six: JgBIAAABKZMUERM3FBITNxM3FBETNxQ2ExMTEhMTExITExQREzcUNhQSEzcTNxQRFDYTExMSExMTNxQRExMTNxQREzcUNhM4EwANBQ==
    seven: JgBIAAABKJMUEhM3ExITNxM3ExMTNxQ2ExITExMSExMTEhMTEzcTNxM3EzcUNhQRFDYUEhQRFBITEhQSExITNxMTEzcTNxM3EwANBQ==
    eight: JgBIAAABKJQTEhQ2FBITNxM3ExITNxQ2ExMTEhMTExIUEhMSEzcTNxMTExITExI4EzcUERMTExITNxQ2FDYUEhMSEzcTNxM3EwANBQ==
    nine: JgBQAAABKJMTExM3FBISOBM3ExITNxQ2FBITEhQSEhMTExITEzcTNxM3FBITEhQ2EzcTExMSExMSExM3EzcTExITEzcUNhM3EwAFNgABKEkTAA0FAAAAAAAAAAA=
    zero: JgBIAAABKJQUERM3FBITNxQ2ExMSOBM3EhMTExITExMSExMSEzcUNxITExITExMSFDYTExQRFBITNxQ2EzcTNxMTEjgTNxM3EwANBQ==
    section12: ZZZ= #DUMMY In Bluetooth romote changed to "myvoice" (Not using IR) 
    lastch: JgBQAAABKZIUEhM3ExITOBI4EhMUNhM3FBITEhMTExITExITFDYTNxMSEzgTNxMSExMSExMTEhMTNxMSExMTNxM3EzcTNxM3EwAFNQABKUkTAA0FAAAAAAAAAAA=
    fastforward: JgBQAAABKpIUERU1FREUNhU1FRAVNRU1FREVEBURFRAVERQRFTUVNRU1FTUVERUQFREVNRUQFREUERQSFDYTNxM3ExIVNRM3FAAFNQABKEkUAA0FAAAAAAAAAAA=
    rewind: JgBQAAABKJMTExI4ExIVNRM3FRETNxM3ExIVERMSExMTEhMTFDYTNxMSFTUTExMSExMSOBMSExMSOBMSEzcTNxU1ExMUNhQ2EwAFNgABKEgTAA0FAAAAAAAAAAA=
    play: JgBQAAABKJMTExM3ExMSNxM4EhMTNxM3ExMTEhMTEhMTEhMTEzcTNxMTEhMTEhMTExITNxMTExITNxM3EzcTOBI4EhMTNxM3EwAFNgABKEkTAA0FAAAAAAAAAAA=
    stop: JgBQAAABKZIVERQ2FBEVNRU1FREVNRU1FRAVERUQFREVEBURFDYUNhQ2FRAVERUQFREVNRQRExMUERU1FTUVNRQ2FREVNRM3FAAFNQABKEgUAA0FAAAAAAAAAAA=
    vod: JgBQAAABKJMTExQ2FRAVNRM3ExMTNxM3ExITExMSExMTEhMTEzcVNRM3ExITExQREzcVERQ2ExITExM3EzcTNxMSEzcTExM3EwAFNgABKEkSAA0FAAAAAAAAAAA=
    myrec: JgBQAAABKJMVERM3ExIUNhM3ExMTNxM3ExITExMSExMTEhMTEjgUNhM3EzcTEhMTEzcTEhM3FBITEhMTEzcTNxUQFTUTExM3EwAFNgABKEgTAA0FAAAAAAAAAAA=
    netflix: JgBQAAABKJMTExM3ExITNxQ3EhMTNxM3ExMSExMTEhMTEhMTEzcTNxQRExMTEhMTFDYTEhM3ExMTNxM3EzcTNxMTEjgTEhM3EwAFNgABKEkTAA0FAAAAAAAAAAA=
    youtube: JgBQAAABKJMTExM3ExIUNhM3ExMTNxQ2ExITExMSExMTEhMTEzcTNxMSEzcTExMSEzcTExM3ExIUNhQSEzcUNhQREzcUEhQ2EwAFNgABKEgTAA0FAAAAAAAAAAA=
    channelup: JgBIAAABKZEVEhM3FBITNxM3ExIUNhQ2FBITEhQSExIUEhMSFDYUNhQ2FBITEhQSExIUERQSFBEUEhQ2FDYUNhQ2FDYUNhQ2FAANBQ==
    channeldown: JgBQAAABKJQUERU1FREVNRQ2FRAVNRU1FREVEBURExIVERQRFTUVNRURFDYUERURExIVERQRFRAVNhQRFTUVNRU1EzcVNRU1FQAFNAABKkcVAA0FAAAAAAAAAAA=
    home: JgBQAAABKJMTExI4ExITNxM3ExMTNxM3ExITExMSExMSExMTEjgTNxMSFRESExMTEjgSOBI4ExITNxQ2FTUTNxMTExITExM3EwAFNgABKEgTAA0FAAAAAAAAAAA=
    back: JgBQAAABKZIUEhM3FBETNxM3ExMTNxM3ExITExMSFBITEhMTEzcTNxM3ExIUNhMTExITExM3ExITExM3ExITNxQ2FDcTEhM3EwAFNgABKUgSAA0FAAAAAAAAAAA=
    circle: JgBQAAABKJMTExM3ExITNxM3FBITNxM3ExITExMSExMTEhMTEzcUNhM3FBETExQRFDYTNxQ3EhMTEhQ3EjgSOBMSExMTEhM3EwAFNgABKUgTAA0FAAAAAAAAAAA=
    left: JgBYAAABKZMVEBQ2FBIVNRQ2FREUNhQ2ExITExQRFBEVERUQFTUVNhQRFTUVERQRFRAVERU1FBEVNRURFTUVNRU1FTUVERU1FQAFNAABKUcVAAxSAAEpSBUADQU=
    right: JgBQAAABKZMTEhM3ExMSOBM3ExITNxM3FBITEhMTExIUEhITEzcUNhM3FDYUEhQRFBITEhM3ExMTEhMTEzcTNxM3EzcUERM3EwAFNgABKEkUAA0FAAAAAAAAAAA= 
    top: JgBQAAABKJQTEhM3ExMTNxM3ExITNxM3FBITEhMTExITExMSFDYUNhQSExITExMSExMSExM3ExMSOBI4EzcTNxM3EzcTEhM3EwAFNgABKUgTAA0FAAAAAAAAAAA=
    bottom: JgBQAAABKJQUERM3FBITNxM3ExITOBI4EhMTExMSExIUEhMSEzcTNxM4ExITEhMTExIUEhM3ExITExQ2EzcUNhQ2EzcUEhI4EwAFNgABKEgTAA0FAAAAAAAAAAA=
    ok: JgBQAAABKJQSExM3ExMSOBM3ExITNxM3ExMTEhMTEhMTExITEzcTNxMTEhMTNxMTEhMTEhM4EhMTNxM3ExMSOBI4EzcTEhM3EwAFNgABKEkTAA0FAAAAAAAAAAA= 
```


# Contribution
if you want to add your own remote template, you can do it in a new folder near the 'simple' and 'lg' remotes and
set remote_template to the name of your new folder. 
just make sure you are changing the html and css methods suffixes

#you are also welcome to contribute new templates. you can add new buttons and remove buttons, just make sure their id matches the id you put in the yaml#



# Latest fix
fixed for 0.92 +
please update JS file, remove broadlink_entity from the settings and add broadlink_host with your broadlink ip
