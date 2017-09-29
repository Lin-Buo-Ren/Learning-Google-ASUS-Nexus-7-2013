# Learning Google(w/ASUS) Nexus 7(2013)
<https://github.com/Lin-Buo-Ren/Learning-Google-ASUS-Nexus-7-2013>

## License
This content is shared-knowledge that released to Public Domain.

This content may contain other parties intellectual property, which is not licensed and keep it as-is.

## Project Codename
flo

## Fastboot OEM commands
### Overview
Command Name | Command Parameters | Command Usage
:---: | :---: | :---: |
uart-on | N/A | Assumed to enable on-board UART on next reboot
uart-off | N/A | Assumed to disable on-board UART on next reboot
unlock | N/A | Unlock bootloader after erasing previous user data
device-info | N/A | Check software state on the device, assumed to be use for warranty check(evil)

### Details
#### device-info
```
$ fastboot oem device-info
...
(bootloader)    Device tampered: false
(bootloader)    Device unlocked: false
(bootloader)    SB=Y
OKAY [  0.005s]
finished. total time: 0.005s
```

NOTE: On Nexus 7 it seems that this check is not enabled, as even the device's bootloader is unlocked the Device tampered/unlocked indicator still spills false.
