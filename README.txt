==============================================================================
 SM-T113 (Galaxy Tab 3 Lite / Tab E 7.0, goyavewifi) - LineageOS 16
 Clean and Broken Files Package - Version: 17.11.2026
==============================================================================

DOWNLOAD
  The files are in the "Releases" section of this repository:
  https://github.com/DrBayStock/SM-T113-LineageOS16-Fix/releases

FILES
  A-TEMIZ(CLEAN)-lineage-16.0-20260901-UNOFFICIAL-goyavewifi-T113FIX-20261117.zip
       CLEAN: Full ROM with all fixes already built in. Install it on its own.
  B1-ORIJINAL-BOZUK(ORIGINAL-BROKEN)-lineage-16.0-20260901-UNOFFICIAL-goyavewifi.zip
       BROKEN: The original LineageOS 16 ROM, unmodified.
       On its own it has problems on this tablet (camera, Wi-Fi, lock-screen touch...).
  B2-DUZELTME(FIX)-T113-LOS16-FixPack-20261117.zip
       FIX: Fix pack flashed ON TOP OF B1. Turns B1 into the clean version.
  README.txt     - this file
  BENIOKU.txt    - Turkish description

  A and "B1 + B2" give the same result. Install whichever you prefer.

INSTALLATION (TWRP)
  First: TWRP > Wipe > Advanced Wipe: wipe System, Data, Cache, Dalvik.

  OPTION A - Clean ROM (easiest)
    1. Install: A-TEMIZ(CLEAN)-lineage-16.0-20260901-UNOFFICIAL-goyavewifi-T113FIX-20261117.zip
    2. Optional: GApps (ARM, Android 9.0, pico/nano recommended)
    3. Reboot System.

  OPTION B - Broken original + fix
    1. Install: B1-ORIJINAL-BOZUK(ORIGINAL-BROKEN)-lineage-16.0-20260901-UNOFFICIAL-goyavewifi.zip
    2. Install: B2-DUZELTME(FIX)-T113-LOS16-FixPack-20261117.zip
    3. Optional: GApps (ARM, Android 9.0, pico/nano recommended)
    4. Reboot System.
    (B2 can also be flashed over an existing B1 install without wiping.)

  - First boot takes a little longer (a 384 MB swap file is created, ~25 s).
  - "Zip signature verification" must be OFF in TWRP.

FIXED ISSUES

  Camera
   - The rear camera works (with the ROM's own kernel the camera sensor was not
     detected at all).
   - Correct image orientation; video recording works.

  Camera app
   - The camera hardware WORKS with this pack. However, the ROM's built-in Camera app
     may be disabled or hidden:
        Settings > Apps > All apps > Camera > Enable
     If it still won't open, download and install a camera app separately
     (e.g. LineageOS Snap or Open Camera).

  Wi-Fi
   - On a clean install Wi-Fi would not turn on at all; it is now set up automatically
     on first boot.
   - Screen casting to a TV (Miracast / Wi-Fi Direct) is enabled: both video and audio
     go to the TV (tested with an Arcelik TV).
   - While the screen is off, unneeded network broadcasts are filtered, so the tablet
     sleeps better and uses less battery.

  Touchscreen
   - Touches land in the right place (rotated to match the screen orientation).
   - Fixed the touchscreen freezing on the lock screen after turning the screen off
     and on (previously only a reboot or opening the camera helped).

  Display
   - Fixed display freezes.
   - Fixed the graphics crash when the screen turns off.
   - The lock screen also auto-rotates.
   - "Ambient display" is turned off on first boot: on this tablet the screen did not
     switch off fully but stayed lit at low brightness, draining the battery.
     (It can be turned back on in Settings > Display.)

  Auto-rotate
   - Accelerometer orientation fixed; the screen rotates correctly.

  Bluetooth
   - Fixed version of the Bluetooth app.

  Battery and sleep
   - The tablet stays in deep sleep longer with the screen off.
   - Disabled the ROM's debug logger that kept writing logs to storage in the background.

  Speed and memory
   - 384 MB swap: fewer apps get killed on 1 GB of RAM.
   - Apps are compiled in the background while charging, so they open faster over time.

  Other
   - adb / USB debugging works properly; the tablet can be used without problems as a
     development and test device with Android Studio.
   - Unneeded phone (SIM) service disabled, since this is a Wi-Fi tablet.
   - Apps can write to shared storage (Internal storage).
   - Fixed a permission needed by the browser and web-view based apps.
   - Rewritten off-mode charging screen.
   - TWRP is no longer overwritten by Samsung's stock recovery.

TECHNICAL NOTE
  So that the camera can work, A and B2 write the LineageOS 15.1
  kernel (Linux 3.10.108) to the boot partition. This combination has been tested on
  this tablet.

KNOWN LIMITATIONS
  - If your router pings connected devices frequently (some "smart" routers do so
    every 15 s), the tablet wakes up more often; this cannot be blocked on the tablet.
  - The Wi-Fi radio listens to every beacon while asleep (old driver limitation).

Use at your own risk. Making a backup before installing is recommended.
