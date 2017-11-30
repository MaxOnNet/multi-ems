# multi-ems

"multi-channel EMS" with Processing and Arduino.  
Simultaneous output of maximum of 20 channels are available.  
The board is designed for ["Human Augmentation Summer School 2017."](https://humanaugmentation.jp/summerschool2017/)  
Permissions are required for any other personal usage.  
Note that the work is still in progress.

## Description

The Processing sends serials to a master Arduino.  
We currently recommend to use the analog version.  

- ems_analog:  
  Control voltage by analog output.  

- ems_digital:  
  The master Arduino communicates with the slave Arduino via I2C.
  Control voltage by digital output.  
  
One board has 4 output channels.  
However, the channels can be increased by using multiple boards.  
In this case, minor revision is required for the source codes.



## Files

- ems_analog
  - emsFace_v3: The Processing code - GUI - v3
  - emsFaceArd_v3: The Arduino code  

- ems_digital
  - emsFacev2: The Processing code - GUI - v2
  - emsFaceArd_2: The master Arduino for EMS pulse generation
  - wire_ems: The slave Arduino for voltage adjusting pulse generation (500 Hz max)
  - wire_ems_time (recommended): The slave Arduino for voltage adjusting pulse generation (500 Hz max), gradually increase the output voltage




## Board Detail

![boardinfo](https://user-images.githubusercontent.com/22442291/30726366-4db8ca26-9f85-11e7-8a8a-daeab15c35e7.jpg)



## Authors

Michinari Kono, U-Tokyo ( mkono50529[at]gmail.com )

Acknowledgements for Keisuke Shiro, Yoshio Ishiguro, Takashi Miyaki, and Jun Rekimoto for assisting the work for both current and prior versions.


## Read Before Use

- Use only under confident understandings of EMS. 
  - You can see details from other great projects [here.](https://github.com/PedroLopes/openEMSstim)
- The board and softwares are NOT medically approved. Always use the device following author's instruction.
- Do NOT leave the power on when it is not in use.
- Do NOT place electrodes to dangerous parts of the body. E.g., around the chest/heart.
- Take care of the output voltage. 
- See LICENCE.
- Follow the Liabilirt Waiver before usage.


## Developing your own Board

Note that there are some errors in the .brd and .sch data (to be fixed).  
- The transistor should be attached the opposite way.
- Model number differs in the .sch (follow the partslist.txt).


## Liability Waiver

Please follow and check the following [liability waiver](https://github.com/PedroLopes/openEMSstim/blob/master/documentation/liability_waiver.md) before usage.


##  Future Work and Areas of Improvement

- The board can be upgraded and become much smaller by surface mounting.
- The components are not limited to the things indicated in the partslist.txt. The board can modified to be much more cheaper/smaller.
- The voltage changes exponentially. 
- The name of the board/repository is temporal.
- My original purpose of the board was to apply EMS to the face. This is why some of the file names are names something including the term ``face.'' These are to be renamed in future updates.  
  
  
## Licence   
  
Copyright (c) 2017 Michinari Kono  
Released under the MIT license  

