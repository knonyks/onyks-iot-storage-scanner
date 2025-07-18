# ONYKS IoT Inventory Scanner

> QR and barcode scanner for tracking and organizing tools and devices.

> "I’ve got two updates about my PCB project—one’s good, the other’s bad. The good news: I’ve finished it. The bad news: I’ve finished it… and it’s currently the world’s most advanced paperweight. Apparently, ‘super high tolerance’ doesn’t mean ‘works perfectly’—who knew? Well, at least it’s got all the pins in the right places... they just don’t do anything useful."

<br />
<br />

## INFO

### Voltage Supply

We gonna use 1.8V logic for cammera with its internal voltage regulator for 1.5V. Thus there is no need for 1.5V DC-DC buck.

Also ESP32S3 offers posibility to use 1.8V I/O logic voltage, however it's configurable for whole GPIO, so it's necesssary to use logic converter 1.8V to 3.3V (or 5V) for display. Main reason for that its conv for two lines instead of 8 lines for cammera communication.

---

## TODO
- [x] Picking elements
- [x] Basic scheme for ESP32
- [x] Scheme for camera connector
- [x] Ensure compatibility of IO voltage for camera with internal flash voltage regulator
- [x] logic converter 1.8V to 3.3V (for display)
- [x] Scheme for display connerctor
- [x] Scheme for usb 
- [x] Scheme for DC-DC buck-boost converter (probably TPS63021)
- [x] Scheme for DC-DC buck converter from 3v3 to 1v8
- [x] Scheme for DC-DC buck converter from 3v3 to 2v8
- [ ] ~~Scheme for DC-DC buck converter form 3v3 to 1v5~~
- [x] Scheme for battery charging
- [x] Battery protection
- [x] Calculate total power demand
- [x] Ensure correct time sequence for voltage suppies (boot: first DOVDD=1.8V, next AVDD = 2.8V, for turn off in reverse - optional)
- [ ] Properly connect cammera to esp32 pins
- [ ] Properly connect display to esp32 pins
- [ ] Properly connect enable of logic converter to esp32 pins
- [ ] Idea of power saving / sleep mode for voltage supply