# A demo Mongoose OS firmware for C/C++

## Overview

This is an demo app, serves as a skeleton for building Mongoose OS
apps from scratch in C/C++.

This app publishes events from an esp32 to a Google Cloud - IOT Core device registry & pubsub

How to run this:
1. setup your device drivers    
2. plug in your device    
3. ensure you can see the device node     

`/dev/cu.SLAB_USBtoUART`


4. build and flash the firmware: 
```bash
$ mos build
$ mos flash
$ mos gcp-iot-setup --gcp-project ${GOOGLE_PROJECT} --gcp-region us-central1 --gcp-registry ${iot_registry}
$ mos wifi ${SSID} ${WIFI_PASSWORD}
```

5. open the serial console:    
```bash
$ mos console
```

6. start your PubSub subscriber application

---
