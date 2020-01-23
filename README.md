Backports openwrt-19.07(kernel 4.14) ramips mt7621 ethernet drivers to chaos_calmer(kernel 3.18).

step1:git clone https://github.com/syb999/mtketh 

step2: cd /chaos_calmer/target/linux/ramips/files/drivers/net/ethernet/ralink/

step3: rm *

step4: cp /mtketh/* /chaos_calmer/target/linux/ramips/files/drivers/net/ethernet/ralink/

step5: cp /mtketh/mt7621-config/config-3.18 /chaos_calmer/target/linux/ramips/mt7621/


step6: cp /mtketh/mt7621-config/mt7621.dtsi /chaos_calmer/target/linux/ramips/dts/

make menuconfig && make V=99


