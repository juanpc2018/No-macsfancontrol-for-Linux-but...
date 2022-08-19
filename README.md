If you have a Mac, one of the best advantages over other machines,
was the software MacsFanControl from Crystalidea,
for Windows and OSX.
it allows to manually control Fan speed on a Laptop!, 
also allows to control fans in MacPro 5,1 2010 and many other Macs.

Macs are designed to be Silent Mode = very slow attack rising speed fan curve.

but there is No macsfancontrol for Linux,
has been asked many times to Crystalidea but they refuse to build for Linux.

anyway... it does Not matter.
for Linux there are several aternatives:

lm-sensors "$ sensors"
fancontrol
mbpfan "a nice option"
macfanctld "had some errors in 22.04.1 LTS"

applesmc-isa-0300
for MacPro 5,1 2010 single CPU tray.

problem is that Default min speed is 2000 for some SMC,
you need to manually Edit with Tea, Kate, or anyother text editor...
fan1_label
PCI
fan1_min
600

fan2_label
PS
fan2_min
600

fan3_label
Intake
fan3_min
600

fan4_label
Exhaust
fan4_min
600

fan5_label
Boosta
fan5_min
1000

where?
/sys/devices/platform/applesmc.768/

the problem is that you need SU

$ sudo is not enough
if you dont have a SU password "probably", you need to 

$ sudo -i
passwd
or
$ sudo passwd root

also
chmod 666 fan*
or 665
maybe:
chown root:root
or 
chown ($whoami):($id -g -n)

Those files are hard to edit.
Not as pretty as MacsFanControl but works.


Boosta A in a Dual CPU tray or Boosta in single CPU tray,
controls a small fan that cools the X58 IC in Single CPU Tray, and 5520 IC in Dual CPU tray.
that IC runs Hot, 
a vacuum clean, and thermal paste change is recommended,
BUT... the plastic retainers / standoffs breat very easy.
can be replaced with 2x small M1 M2 M3 maybe & 20mm long screws, and a plastic / Kapton O-ring washer in the back of the PCB.
does Not need to be tight, springs are strong, just balanced.
a lock nut or a small amount of nail paint or a drop of super glue will hold the screw in place.
do not over tight, the sprin must have room to move.

