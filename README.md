# linux_help

# Install wifi adapter drivers

https://superuser.com/questions/1401954/how-to-config-realtek-rtl8101-2-6e-pci-express-fast-gigabit-ethernet-wi-fi-on

# Now create a udev rule:

    $ sudo gedit /etc/udev/rules.d/51-android.rules
    SUBSYSTEM=="usb", ATTR{idVendor}=="22b8", ATTR{idProduct}=="2e81", MODE="0666", GROUP="plugdev"
    
  <b>Now the device is good to be detected once udev rule is reloaded. So, let's do it:</b>
  
    sudo udevadm control --reload-rules
