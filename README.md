# Installing UGS

Install `openjdk-8-jre` package and make sure version 8 is the default for the system.

```
sudo apt install openjdk-8-jre
sudo update-alternatives --set java /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java
```

Get latest release: https://winder.github.io/ugs_website/download/

```
cd ~
unzip ~/Downloads/ugs-platform-app-2.0-SNAPSHOT.zip
ln -s ~/ugsplatform/bin/ugsplatform ~/bin/ugsplatform
```

# Flashing

```
avrdude -v -p avmega2560 -U flash:w:grbl_mega.hex:i -c wiring -P /dev/ttyACM0 -D
```

## Default settings

```
$0=10
$1=255
$2=0
$3=0
$4=1
$5=0
$6=0
$10=1
$11=0.010
$12=0.002
$13=0
$20=0
$21=1
$22=0
$23=0
$24=35.000
$25=800.000
$26=200
$27=4.000
$30=12000
$31=0
$32=0
$100=57.288
$101=57.288
$102=200.000
$110=16510.000
$111=16510.000
$112=4570.000
$120=1470.000
$121=1470.000
$122=700.000
$130=889.000
$131=889.000
$132=128.000
```

## My Tweeked Settings

```
$0 = 10    (Step pulse time, microseconds)
$1 = 255    (Step idle delay, milliseconds)
$2 = 0    (Step pulse invert, mask)
$3 = 2    (Step direction invert, mask)
$4 = 1    (Invert step enable pin, boolean)
$5 = 0    (Invert limit pins, boolean)
$6 = 0    (Invert probe pin, boolean)
$10 = 1    (Status report options, mask)
$11 = 0.010    (Junction deviation, millimeters)
$12 = 0.002    (Arc tolerance, millimeters)
$13 = 0    (Report in inches, boolean)
$20 = 1    (Soft limits enable, boolean)
$21 = 1    (Hard limits enable, boolean)
$22 = 1    (Homing cycle enable, boolean)
$23 = 1    (Homing direction invert, mask)
$24 = 50.000    (Homing locate feed rate, mm/min)
$25 = 800.000    (Homing search seek rate, mm/min)
$26 = 200    (Homing switch debounce delay, milliseconds)
$27 = 5.000    (Homing switch pull-off distance, millimeters)
$30 = 12000    (Maximum spindle speed, RPM)
$31 = 0    (Minimum spindle speed, RPM)
$32 = 0    (Laser-mode enable, boolean)
$100 = 57.288    (X-axis travel resolution, step/mm)
$101 = 57.288    (Y-axis travel resolution, step/mm)
$102 = 200.000    (Z-axis travel resolution, step/mm)
$103 = 13.333
$110 = 16510.000    (X-axis maximum rate, mm/min)
$111 = 16510.000    (Y-axis maximum rate, mm/min)
$112 = 4570.000    (Z-axis maximum rate, mm/min)
$113 = 15000.000
$120 = 1470.000    (X-axis acceleration, mm/sec^2)
$121 = 1470.000    (Y-axis acceleration, mm/sec^2)
$122 = 700.000    (Z-axis acceleration, mm/sec^2)
$123 = 4000.000
$130 = 889.000    (X-axis maximum travel, millimeters)
$131 = 889.000    (Y-axis maximum travel, millimeters)
$132 = 128.000    (Z-axis maximum travel, millimeters)
$133 = 360.000
```