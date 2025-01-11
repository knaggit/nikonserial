# nikonserial
Research on the serial protocol used in Nikon film cameras like the **F5**, **F6**, **F90**, **F100**.

# What?

Some Nikon film cameras (like F5, F6, F100 ...) allow you to save settings (ISO, aperture, lens ...) for each shot to an internal storage. You can compare that to modern EXIF metadata, but it's not the same technically. Nikon also sold an external device to save that data onto a CF card called MV-1. It's now very hard to get such a thing for a reasonable price.

# Why?

If you digitalise your film rolls you won't have that data anymore but the settings used by your scanner/camera. If you have written down your settings for each shot you can manually edit the EXIF data to show the "proper" values.

* Nikon MV-1 Adapters are (in 2025) around 400-500 $
* [Meta 35 (USB)](https://promotesystems.zendesk.com/hc/en-us/articles/360061330171-Purchase-a-Meta-35) project is discontinued and there are no options to get one anymore

# How?

The Nikon cameras in question have a 10-pin connector used for remote releases. It also features a TTL serial port. Voltage levels are at 5V.
Documentation about the serial port is not readily available, you can see some links in the last section. There are tools available for readout like "Camera Companion" and SoftTALK. Both are closed source programs. I have not found a Linux (or open source alternative).

# Hardware

## Known Cables
They are all discontinued
* [HarTALK](https://www.cocoon-creations.com/COCOON-NiCommHarTALK.shtml)
* [Nikon MC-31 (DB-25 serial port)]
* [Nikon MC-33 (DB-9 serial port)](https://www.mir.com.my/rb/photography/hardwares/classics/NikonF5/accessories/PhotoSecretary/index.htm)
* [DataCable-2](https://www.schneordesign.com/diy/diy-photography/buy-data-cable-2/)

## DIY
There is no need to buy special hardware, a cheap FTDI or similar USB-to-Serial device will work. Connect RX to TX and vice versa and GND to GND. If you have a voltage selector, use 5V. 3V3 might work, it did not for me.

### Explaining 10 pin connector
* [schneordesign.com](https://www.schneordesign.com/diy/diy-photography/f100-concept/)
* [photo.geneste.free.fr](https://photo-geneste-free-fr.translate.goog/technique/index.html?_x_tr_sch=http&_x_tr_sl=auto&_x_tr_tl=de&_x_tr_hl=en-US&_x_tr_pto=wapp)
* [archive.org](https://web.archive.org/web/19981207005100/http://members.aol.com/khancock/pilot/nbuddy/protocol.html)

### Software (Win 2000 & XP)
* [holymoose.com (Camera Companion)](https://www.holymoose.com/ccstart.html)
* [cocoon-creations.com (SoftTALK 2000)](https://www.cocoon-creations.com/COCOON-NiCommSoftTALK-98.shtml#anchor2735385)
