If you have a Mac, one of the best advantages over other machines,
was the software MacsFanControl from Crystal idea,
for Windows and OSX.
it allows to manually control Fan speed on a Laptop!, 
also allows to control fans in MacPro 5,1 2010 and many other Macs.

but there is No macsfancontrol for Linux,
has been asked many times to Crystalidea but they refuse to build for Linux.

anyway... it does Not matter.
for Linux there are several aternatives:

lm-sensors "$ sensors"
fancontrol
mbpfan "a nice option"
macfanctld "had some errors in 22.04.1 LTS"

applesmc-isa-0300
for MacPro 5,1 2010

problem is that Default min speed is 2000 for some SMC,
you need to manually Edit with Tea, Kate, or anyother text editor...
fan1_min
600
fan2_min
600
fan3_min
600
fan4_min
600
fan5_min
1000
fan5_label
Boosta

where?
/sys/devices/platform/applesmc.768/

the problem is that you need SU
#
$ sudo is not enough
also
chmod 666 fan*
or 665
maybe:
chown root:root
or 
chown ($whoami):($id -g -n)

Those files are hard to edit.
Not as pretty as MacsFanControl but works.
