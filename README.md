# avsdpll_3v3 - OnChip PLL Clock Multiplier 


### Specifications
    - ClockIn  5MHz  to 12.5MHz  at 1.8v
    - ClockOut 40MHz to 100MHz   at 1.8v
    - 8x multiplication
| Parameter | Description                      | min  | typ  | max   | Unit | Condition                                                                            |
|-----------|----------------------------------|------|------|-------|------|--------------------------------------------------------------------------------------|
| VDD       | Digital supply voltage           |      | 1.8  |       | V    | T=-40 to 150C                                                                        |
| FCLKREF   | Reference clock frequency        | 5    | 10   | 12.5  | MHz  |                                                                                      |
| FCLKOUT   | Output clock frequency           | 41.6 | 79.1 | 99.82 | MHz  | PLL mode, T=27C, VDD=1.8                                                             |
| FCLKOUT   | Output clock frequency           | 6    |      | 251   | MHz  | VCO mode, T=27C, VDD=1.8                                                             |
| DC        | Duty Cycle                       | 50.8 | 52.4 | 53.7  | %    | T=-40 to 150C                                                                        |
| VVCO      | Oscillator control input voltage | 0.5  |      | 1.2   | V    |                                                                                      |
| TSET      | Settling time                    | 3.8  | 8    | 8     | us   | start from EN_CP and report 2 values; one at FCLKOUT=40MHz and one at FCLKOUT=100MHz |

This repository hosts relevant files on the IP.


## 1. Contents
00. [Specifications](https://github.com/eddygta17/avsdpll_3v3/tree/master/00.Specifications) - Specifications provided for the PLL.
01. [Reports](https://github.com/eddygta17/avsdpll_3v3/tree/master/01.Reports) - Reports and presentations.
02. [Schematic](https://github.com/eddygta17/avsdpll_3v3/tree/master/02.Schematic) - Schematic of different components.
03. [Layout](https://github.com/eddygta17/avsdpll_3v3/tree/master/03.Layout) - Layout of different components.
04. [Misc](https://github.com/eddygta17/avsdpll_3v3/tree/master/04.Misc) - Images

## 2. Pre-layout Simulation of PLL 
1. Input Frequency (F_in) = 5MHz
#### Locking in
![](04.Misc/Fin5.png)
#### 8x clock
![](04.Misc/Fclose5.png)
2. Input Frequency (F_in) = 10MHz
#### Locking in
![](04.Misc/Fin10.png)
#### 8x clock
![](04.Misc/Fclose10.png)


## 3. Layout
### PFD
![](04.Misc/lay_pfd.png)
### VCO
![](04.Misc/lay_vco.png)
### DIV2
![](04.Misc/lay_div2.png)
### DIV8
![](04.Misc/lay_div8.png)

__Due to the limitaions of OSU180 the chargepump layout was not made.__

## 4. Post-layout Simulation of PLL 
1. Input Frequency (F_in) = 5MHz
#### Locking in
![](04.Misc/FLin5.png)
#### 8x clock
![](04.Misc/FLclose5.png)
2. Input Frequency (F_in) = 10MHz
#### Locking in
![](04.Misc/FLin10.png)
#### 8x clock
![](04.Misc/FLclose10.png)




## 6. Tools Used

1. [Ngspice](http://ngspice.sourceforge.net/download.html)
2. [magic](http://opencircuitdesign.com/magic/)

## 7. Future work

1. Porting this IP to SKY130.
2. Improve area efficiency.
3. Add biasing current.
4. Improve jitter and lock in time.


## 8. Author
- Abel Joseph John, B.Tech in ECE, NSS College of Engineering, Palakkad


## 9. Acknowledgments & Thanks
- Kunal Promode Ghosh, for mentoring and guidance.
- Philipp Gühring, for helping out with tools.
- R. Timothy Edwards, for creating awesome OpenSource tools.
- Prof. R Jacob Baker, for his textbook on CMOS design.



