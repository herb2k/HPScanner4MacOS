# HPScanner4MacOS
Restore your HP Scanner functionality on MacOS Big Sur and higher, without relying on HP Smart and other Applications!

Tested using an HP Photosmart 5510d with Scanner capability over AirPrint, using Ventura 13.0 and a clean install of Sonoma 14.4.

### 1. Download the HP 5.1.1 Printer Software Update from Apple
[HP 5.1.1 Printer Software Update](https://support.apple.com/en-ca/106385)

Note: File is 585MB!

### Update: This will not install above macOS 15.0.0 

Please download ```Payload.zip``` from the releases section and copy the contents of the extracted ```Library``` subfolder to their respective locations in ```/Library/Printers``` and ```/Library/Image Capture```.

If asked to merge or overwrite, always merge!

### For macOS 26 Tahoe: 

You will encounter gatekeeper warnings, and you will need to run a series of ```xattr -d com.apple.quarantine <file_name>``` (the names and locations will be different depending on your printer) will need to be run if 'Open Anyway' under the 'Privacy and Security' Settings Section does not work. 

If you are using an Apple Silicon device, Rosetta needs to be installed (macOS will prompt you to do this)

### 2. Install Image Capture Support Apps
Extract ```Devices.zip``` from this repo, you will have 3 apps extracted.

These are apps/plugins that enable the scanner functionality in macOS.

Copy:
```
HP M1130_M1210 Scanner.app
HP Scanner 3.app
HPScanner.app

to /Library/Image Capture/Devices
```
### 3. Install your printer driver
For a wireless printer, choose the driver from the package and not the auto-detected one).

This may take a couple of tries. In my case, the Driver version is 4.2.5 while the basic macOS driver version is 2.x or 3.0x

You can verify it works correctly by opening System Information > Printers and looking for a line that reads ```'Scanning Support: Yes'```

### 4. REBOOT
A reboot is necessary to have the scanner show up in Image Capture.

### 5. Open Image Capture
Open Image Capture, with your printer/scanner powered on and you should see it in the left under 'Shared Devices'. 
Select it, and an Overview scan should be automatically performed. 


### 6. macOS Ventura (13) and higher
If you see a pop up from Image Capture that says "HP Scanner 3" (or similar) is damaged:

You may need to double click each of the 'Devices' apps in `/Library/Image Capture/Devices` one at a time and click "Open Anyway" under Settings > Privacy.
