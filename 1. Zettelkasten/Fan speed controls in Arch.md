070520240108
Status: #idea
Tags: 

# Fan speed controls in Arch
- For my asus laptop some useful links -
	- Directory of the file --> `/sys/devices/platform/asus-nb-wmi/hwmon/hwmon4/pwm1_enable`
	- [Check arch wiki](https://wiki.archlinux.org/title/Fan_speed_control)

```
sysfs attributes
----------------

pwm[1-5] - this file stores PWM duty cycle or DC value (fan speed) in range:
       0 (lowest speed) to 255 (full)

pwm[1-5]_enable - this file controls mode of fan/temperature control:
    * 0 Fan control disabled (fans set to maximum speed)
    * 1 Manual mode, write to pwm[0-5] any value 0-255
    * 2 "Thermal Cruise" mode
    * 3 "Fan Speed Cruise" mode
    * 4 "Smart Fan III" mode (NCT6775F only)
    * 5 "Smart Fan IV" mode

pwm[1-5]_mode - controls if output is PWM or DC level
        * 0 DC output
        * 1 PWM output
```



___
## References
