# Seznam součástek pro Mars rover
## Motor
### 25GA-370
- [Datasheet](https://www.tronsunmotor.com/data/upload/file/201910/e78fcf93ed604a64c69852b5db49a03f.pdf)
- [🛒 Dratek.cz](https://dratek.cz/arduino/123005-motor-jga25-370-12v-130rpm-s-prevodovkou.html)

## Motor driver
### TB6612FNG
- malý (2×2 cm)
- dual motor
- spotřebuje 7 pinů ovládání (2×PWM, 4×IN) + standby pin
- potřebuje taky VCC, které udává napětí komunikace
- nemá heat sink, vysoká efektivita, velmi málo energie se převádí na teplo
- standby low - úsporný režim
- vstup do 15 V
- [Pinout](https://cdn.sparkfun.com/assets/parts/3/1/5/7/09457-04.jpg)
- [Datasheet](https://toshiba.semicon-storage.com/info/datasheet_en_20141001.pdf?did=10660)
- [🛒 AliExpress](https://www.aliexpress.com/item/32465698640.html)

## Microcontroller
### ESP-32 (CP2102 USB-C)
- [Pinout](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/_images/esp32-devkitC-v4-pinout.png)
- [Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-wroom-32_datasheet_en.pdf)
- [🛒 AliExpress](https://www.aliexpress.com/item/4000090521976.html) (+ i pěkný terminal adapter)

## Kamera
### ESP-32 CAM
- je i s hezkou boardou - jde připojit na micro USB
- OV2640 kamera (1600×1200=2Mpix)
- 15 FPS
- nebudeme moci použít bluetooth, je na streamovaní videa moc pomalý
- built-in ledka (miniblesk)
- [Pinout](https://lastminuteengineers.com/wp-content/uploads/iot/ESP32-CAM-Pinout.png)
- [Datasheet](https://loboris.eu/ESP32/ESP32-CAM%20Product%20Specification.pdf)
- [🛒 AliExpress](https://www.aliexpress.com/item/1005003472117545.html)

## Napájení
většinu napájení bohužel nemůžeme objednat v Číně, protože by to nedošlo v rozumném čase 
### Baterie (mé návrhy)
<!-- https://www.rcprofi.cz/akumulatory-li-pol.html?orderby=0&cenado=5633&asistentatrib[160][1132]=1132&asistentatrib[161][1140]=1140&asistentatrib[161][1141]=1141&asistentatrib[199][2115]=2115 -->
#### 1. KAVAN Li-Po 3700mAh 11.1V
- 3 články
- 3700mAh
- [🛒 RCprofi](https://www.rcprofi.cz/kavan-li-po-3700mah-11-1v-40-80c-41-1wh)
- [🛒 MojeRC](https://www.mojerc.cz/144017/kavan-li-po-3700mah-11-1v-40-80c-41-1wh)
#### 2. KAVAN Li-Po 4500mAh 11.1V
- 3 články
- 4500mAh
- o ~250Kč dražší
- [🛒 RCprofi](https://www.rcprofi.cz/kavan-li-po-4500mah-11-1v-40-80c-50-0wh)
- [🛒 MojeRC](https://www.mojerc.cz/144019/kavan-li-po-4500mah-11-1v-40-80c-50-0wh)


### Nabíječ SKYRC e680
- potřebujeme nabíječ na lipo baterii
- v balení je i adaptér na XT60 konektor, ke KAVAN bateriím bychom museli dokoupit (viz [XT60 konektorový pár](#xt60-konektorový-pár))
- má převodníkovou destičku pro JST-XH servisní konektor (1 - 6 článků Li-Po)
- [Manuál](https://www.skyrc.com/download/e680_Instruction_Manual_EN_V1.30.pdf)
- [Výrobce](https://www.skyrc.com/Charger/e680)
- [Review](https://youtu.be/zIszpMdlm-I)
- [🛒 RCprofi](https://www.rcprofi.cz/sky-rc-e680-nabijec-80w)
- [🛒 MojeRC](https://www.mojerc.cz/137348/sky-rc-e680-nab%C3%ADje%C4%8D-80w)

### XT60 konektorový pár
- KAVAN baterie nemají XT60 adaptér, museli bychom si napájet svůj
- považováno spíše za výhodu
- [🛒 RCprofi](https://www.rcprofi.cz/xt60-konektor-1par)
- [🛒 MojeRC](https://aliexpress.com/item/1005005681985806.html)

### Ochrana nízkého napětí baterie XH-M611
- ochrana na vybití
- potřebujeme, abychom si baterii nezničili
- 7 - 80V input
- nedá se sehnat v ČR
- [Review](https://youtu.be/P2g-NxdF6d8)
- [🛒 AliExpress](https://www.aliexpress.com/item/1005005681985806.html)

## Regulátor napětí
### LM2596
- step-down
- input 4 - 35V
- output 1.23 - 30V
- s nastavitelnou regulací
- je to levné, koupil bych více, budou se hodit
- [Pinout](https://electrobes.com/wp-content/uploads/2019/05/pinout-of-lm2596-dc-dc-buck-converter-module-adjustable-power-supply-board-in-pakistan.webp)
- [Datasheet](https://www.ti.com/lit/ds/symlink/lm2596.pdf)
- [🛒 AliExpress](https://www.aliexpress.com/item/10000000656280.html)

## Kompas
### GY-271 HMC5883
- [Pinout](https://electropeak.com/learn/wp-content/uploads/2020/09/GY271-Arduino-Pinout.jpg)
- [Datasheet](https://cdn-shop.adafruit.com/datasheets/HMC5883L_3-Axis_Digital_Compass_IC.pdf)
- [🛒 AliExpress](https://www.aliexpress.com/item/1005002525957722.html)

## Akcelerometr
### GY-521 MPU-6050
- [Pinout](https://electropeak.com/learn/wp-content/uploads/2020/11/MPU6050-Pin.jpg)
- [Datasheet](https://invensense.tdk.com/wp-content/uploads/2015/02/MPU-6000-Datasheet1.pdf)
- [🛒 AliExpress](https://www.aliexpress.com/item/32340949017.html)