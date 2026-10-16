This project is a starbie which basically works as a starboy. I made this as part of the half-life program for week 1, with my goal of getting a 3d printer and learning more about hardware. I wanted my first hardware project to also reflect some of my interests so I added some Avatar The Last Airbender elements to it. 

I first started off by creating my schematic. In this step I added all the components that will be added to my starbie. I also attached some GNDs and other tiny components to these bigger components. The picture below is a how the schematic ended up looking like after adding all the components.
<img width="956" height="533" alt="image" src="https://github.com/user-attachments/assets/d4f84a2d-3f5b-4cff-8e30-188eb1faa44a" />

After this was complete, I transferred all the components from my schematic to my PCB editor. The components weren't arranged in the shape that I wanted it to be so I had to move around the components. After everything was moved as I saw fit, I started outlining my starbie on the edge.cuts layer. This took some time as I first started off using the line tool but realised that the polygon tool was much more beneficial. 

<img width="663" height="552" alt="Screenshot 2026-10-10 195928" src="https://github.com/user-attachments/assets/21a3f17a-ad82-4017-b64e-9a889ca12b78" />

After this step, I wired pieces of components to one another by using the F.cu and B.Cu layers depending on the piece. Finally I added a GND zone over my PCB.

<img width="573" height="515" alt="Screenshot 2026-10-10 200655" src="https://github.com/user-attachments/assets/8bc94a3a-726e-4865-ac43-b63e53a8f552" />

(the red layer in the picture is the GND layer and the red/blue lines across my PCB is the routing)

To add some of my design to my starbie I added the following images to my starbie PCB (by using the image converting tool, changing the size, managing footprint libraries, then adding the footprint)

<img width="735" height="902" alt="dd6e50f1661857793c4e3dcc5893c3c0" src="https://github.com/user-attachments/assets/64fd22cd-7f61-4689-b4c5-513e3589861d" />
<img width="736" height="742" alt="5c841f9acfdc52158e563047b8ce2427" src="https://github.com/user-attachments/assets/173f2253-daf8-4c50-a27d-e3aa49c558b5" />
<img width="828" height="1102" alt="79ba63d8b182e5469686890a7913d24a" src="https://github.com/user-attachments/assets/83f281b4-e24a-4e6a-b51a-86861b557d70" />

After converting these images to footprints, I added them onto my PCB:

<img width="642" height="485" alt="image" src="https://github.com/user-attachments/assets/27a93585-7b6e-4537-ab5b-2031ba14ec74" />

To get a better view of how the PCB would look like I went to 3D viewer and viewed my PCB.

<img width="661" height="585" alt="image" src="https://github.com/user-attachments/assets/e4f158f8-355d-457b-8bce-a0d39d0c0c8d" />

Now that my PCB and schematic were finished I moved onto arduino and worked on the code for my starbie. I had to download some libraries first and install the file in the guide then open it in arduino. After that I started editing the code as suited to my needs. 

[{bom}.csv](https://github.com/user-attachments/files/33570499/bom.csv)
<img width="892" height="570" alt="image" src="https://github.com/user-attachments/assets/568ea38c-3489-4fa7-ab41-d970ac39ca2c" />

The image above represents the bill of materials for my project.

| Part | Qty | Unit | Total | Vendor |
| :--- | :---: | :---: | :---: | :--- |
| **XIAO ESP32 C3**<br>_the starbie_ | 1 | $5.00 | $5.00 | [SEEED](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html) |
| **0.96 OLED**<br>_the starbie_ | 1 | $3.25 | $3.25 | [Buy & Display](https://www.buydisplay.com/i2c-yellow-blue-0-96-inch-oled-display-128x64-arduino-raspberry-pi?srsltid=AU7gw4Us8HCG07aa_U77P5M7IeI37yqj1hleT46jM1SQ8ud3P2FK_a0UiIU) |
| **MPU6050**<br>_the starbie_ | 1 | $1.97 | $1.97 | [Alibaba](https://www.alibaba.com/pla/GY-521-MPU-6050-MPU6050-Module-Black-Tantalum_1600213865732.html?mark=google_shopping&biz=pla&searchText=development+boards+kits&product_id=1600213865732&pcy=us_en&src=sem_ggl&field=UG&from=sem_ggl&cmpgn=23943467922&adgrp=200057618520&fditm=&tgt=pla-2486796178070&locintrst=&locphyscl=9010778&mtchtyp=&ntwrk=g&device=c&dvcmdl=&creative=813217375325&plcmnt=&plcmntcat=&aceid=&position=&gad_source=4&gad_campaignid=23943467922&gbraid=0AAAAAD8m77pDztas6Z3pfTujtsSMY8q-Z&gclid=Cj0KCQjwxKfWBhDkARIsAMKwkNZV6KNs3BefRGrQFq_bAq4gqdX8o86dh-3oM10WZ6rZmdwj93Q0SokaAle7EALw_wcB) |
| **DHT11**<br>_the starbie_ | 1 | $1.51 | $1.51 | [RobotShop](https://www.robotshop.com/products/dht11-temperature-humidity-sensor-module-breakout?gad_source=4&gad_campaignid=20145188159&gbraid=0AAAAAD_f_xwvx7Hp_o3AEYOLOBA7buNlX&gclid=Cj0KCQjwxKfWBhDkARIsAMKwkNY6uNE4XTcR25dXlnremtYj_LWe2nqZAIJs_rnb5TkNCBKVBxbT_6saAgUtEALw_wcB) |
| **Switches**<br>_the starbie_ | 4 | $0.40 | $1.60 | [mechanical keyboards](https://mechanicalkeyboards.com/search?q=MX+switch&options%5Bprefix%5D=last) |
| **Keycaps**<br>_the starbie_ | 4 | $0.50 | $2.00 | [Adafruit](https://www.adafruit.com/product/5174) |
| **10k Resistor**<br>_the starbie_ | 1 | $0.20 | $0.20 | [american loopers](https://www.americanloopers.com/products/resistor-10k-ohm?variant=41187979788393&country=US&currency=USD&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic&srsltid=AU7gw4VZZpYUfRKCbqIdtCVOjeBEukuuM9ssWHkhUWcLF4yVjcf8ehaZCy4&com_cvv=8fb3d522dc163aeadb66e08cd7450cbbdddc64c6cf2e8891f6d48747c6d56d2c) |
| **PCB**<br>_the starbie_ | 1 | $10.00 | $10.00 | [JLC](https://www.jlcpcb.com/) |
| **Tax & shipping**<br>_for the whole order_ | - | - | $3.00 | - |

