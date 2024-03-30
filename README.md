# HPScanner4MacOS
Restore your HP Scanner functionality on MacOS Big Sur and higher, without relying on HP Smart and other Applications!

Tested using an HP Photosmart 5510d with Scanner capability over AirPrint.

### 1. Download the HP 5.1.1 Printer Software Update from Apple
https://support.apple.com/en-ca/106385

File is ~530MB

### 2. Extract Devices.zip 
These contain support apps that enable the scanner functionality in macOS.

Copy HP M1130_M1210 Scanner.app, HP Scanner 3, HPScanner to /Library/Image Capture/Devices

### 3. Install your printer driver
For a wireless printer, choose the driver from the package and not the auto-detected one).

This may take a couple of tries. In my case, the Driver version is 4.2.5 while the basic macOS Driver Version is 2.x or 3.0x

You can verify it works correctly by opening System Information > Printers and looking for a line that reads 'Scanning Support: Yes'

### 4. REBOOT
A reboot is necessary to have the scanner show up in Image Capture.
