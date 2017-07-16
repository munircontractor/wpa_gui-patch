## `wpa_gui` patch to default to system tray

The patch file in this repo is built against the source code for `wpa_supplicant` version 2.6.
It changes the default option for `wpa_gui` to start in the system tray, instead of in the main window. I find that to be a more sensible default since in most cases the device will connect to a saved network, and the window pop-up is just downright annoying.

The patch can be applied to the source code through the following commands:

    tar -xf wpa_supplicant-2.6.tar.gz
    cd wpa_supplicant-2.6/
    patch -Np1 -i ../wpa_gui-default-to-tray.patch

The patch also replaces the startup option `-t` with `-w`, which will start the main window. The desktop file and the man page are also edited accordingly.
