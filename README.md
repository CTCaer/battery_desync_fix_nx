# Battery Desync Fix NX


Battery Desync Fix NX app allows you to calibrate your Fuel Gauge IC with values based on your Switch's factory calibration data.


This fixes issues with battery percentage being wrong.

HOS saves them at power off/reboot and restores them at boot.

The issue is theorized to be hardware bug in Fuel Gauge that is triggered by HOS. Basically, it can happen on restore when Fuel Gauge has significantly different values from HOS last saved context.


## How to calibrate your battery:

You **must** run this app **in succession** to your sysMMC and every emuMMC (if they exist). Otherwise the moment you switch to another one, it will desync again.

You can start from whichever you want.

Assuming you start with SYS CFW or OFW/Stock:

```
1. Boot SYS CFW
2. Run the app
3. Press X button for forcing init
4. Exit the app properly (press B)
5. If you want this for OFW, reboot and boot OFW or Stock.
6. Do 2 full charging cycles (??% -> 100% -> 0% -> 100% -> 0%)

- Do not reboot to something else until done!
- When HOS forces a sleep because battery is too low, wake it again and again until it shows red battery icon.
- In case HOS powered off, put charger to enter HOS.
  If it's stuck on black screen and charger icon, unplug/plug after a bit so you can enter inside.
  Do not fully charge in there because it HOS will restore the previous Fuel Gauge context.

```

After it's done, you can repeat the procedure for emuMMC.

**Do not switch in-between SYS, EMU and anything else without finishing the 2 charging cycles.** Always be careful when rebooting until done.


## Disclaimer:

No support is provided for that app at all. Use it at your own discretion!

This app **is not to be included** in packs, app stores, etc. It is a specialized app that must only run if user has real issues with capacity full and percentage.

Easiest way to identify the issue is random up/downs on battery percentage and the capacity now not matching voltage avg/oc.
