# 主板线路连接

## CON1：

| 针脚号 | 功能猜测  | 连接                                     |
| ------ | --------- | ---------------------------------------- |
| 1      | 背光负极  | U8-Pin3 -->R6(12Ω)-->GND                 |
| 2      | 背光正极  | U8-Pin5  & -->D7-->U8-Pin1               |
| 3      | GND       | GND                                      |
| 4      | 3V3       | -->L2-->U5-OUT                           |
| 5      | GND       | GND                                      |
| 6      | GND       | GND                                      |
| 7      | D18       | U1-Pin18  (PD12) (LCD_D18)               |
| 8      | D19       | U1-Pin19  (PD13) (LCD_D19)               |
| 9      | D20       | U1-Pin21  (PD14) (LCD_D20)               |
| 10     | D21       | U1-Pin23  (PD15) (LCD_D21)               |
| 11     | D22       | U1-Pin24  (PD16) (LCD_D22)               |
| 12     | D23       | U1-Pin25  (PD17) (LCD_D23)               |
| 13     | GND       | GND                                      |
| 14     | GND       | GND                                      |
| 15     | D10       | U1-Pin12  (PD6) (LCD_D10)                |
| 16     | D11       | U1-Pin13  (PD7) (LCD_D11)                |
| 17     | D12       | U1-Pin14  (PD8) (LCD_D12)                |
| 18     | D13       | U1-Pin15  (PD9) (LCD_D13)                |
| 19     | D14       | U1-Pin16  (PD10) (LCD_D14)               |
| 20     | D15       | U1-Pin17  (PD11) (LCD_D15)               |
| 21     | GND       | GND                                      |
| 22     | GND       | GND                                      |
| 23     | D2        | U1-Pin06  (PD0) (LCD_D2)                 |
| 24     | D3        | U1-Pin07  (PD1) (LCD_D3)                 |
| 25     | D4        | U1-Pin08  (PD2) (LCD_D4)                 |
| 26     | D5        | U1-Pin09  (PD3) (LCD_D5)                 |
| 27     | D6        | U1-Pin10  (PD4) (LCD_D6)                 |
| 28     | D7        | U1-Pin11  (PD5) (LCD_D7)                 |
| 29     | GND       | GND                                      |
| 30     | LCD_CLK   | -->R23-->U1-Pin26 (PD18) &  -->C62-->GND |
| 31     | 3V3       | -->L2-->U5-OUT                           |
| 32     | LCD_HSYNC | U1-Pin28  (PD20)                         |
| 33     | LCD_VSYNC | U1-Pin29  (PD21)                         |
| 34     | LCD_DE    | U1-Pin27  (PD19)                         |
| 35     | NC        | NC                                       |
| 36     | GND       | GND                                      |
| 37     | RESET     | U13-Pin7                                 |
| 38     | MOSI      | U13-Pin5                                 |
| 39     | CLK       | U13-Pin6                                 |
| 40     | /CS       | U13-Pin3                                 |



## U1:

### PIN 1~22:

| 引脚编号 | 连接                        | 可能的功能      |
| -------- | --------------------------- | --------------- |
| 1        | -->C299-->R59 ...           | Headphone-L OUT |
| 2        | -->C21-->GND                | HPCOMFB         |
| 3        | NC                          | HPCOM           |
| 4        | -->C15-->GND & -->C16-->GND | HPVCC           |
| 5        | -->L2-->U5-OUT              | VCC-IO(3V3)     |
| 6        | CON1-23                     |                 |
| 7        | CON1-24                     |                 |
| 8        | CON1-25                     |                 |
| 9        | CON1-26                     |                 |
| 10       | CON1-27                     |                 |
| 11       | CON1-28                     |                 |
| 12       | CON1-15                     |                 |
| 13       | CON1-16                     |                 |
| 14       | CON1-17                     |                 |
| 15       | CON1-18                     |                 |
| 16       | CON1-19                     |                 |
| 17       | CON1-20                     |                 |
| 18       | CON1-07                     |                 |
| 19       | CON1-08                     |                 |
| 20       | -->L2-->U5-OUT              | VCC-IO(3V3)     |
| 21       | CON1-09                     |                 |
| 22       | -->L1-->U4-OUT              | VDD-CORE(1V1)   |

### PIN 23~44:

| 引脚编号 | 连接                 | 可能的功能                         |
| -------- | -------------------- | ---------------------------------- |
| 23       | CON1-10              |                                    |
| 24       | CON1-11              |                                    |
| 25       | CON1-12              |                                    |
| 26       | -->R23-->CON1-30     | LCD_CLK                            |
| 27       | -->CON1-34           | LCD_DE                             |
| 28       | -->CON1-32           | LCD_HSYNC                          |
| 29       | -->CON1-33           | LCD_VSYNC                          |
| 30       | VCC-DRAM   (U7-OUT)  | VCC-DRAM(2V5)                      |
| 31       | VCC-DRAM   (U7-OUT)  | VCC-DRAM(2V5)                      |
| 32       | VCC-DRAM   (U7-OUT)  | VCC-DRAM(2V5)                      |
| 33       | C1C3C5C6C7；R1R2     | SIP DDR1(内置DDR外接阻容件)        |
| 34       | VCC-DRAM   (U7-OUT)  | VCC-DRAM(2V5)                      |
| 35       | -->L1-->U4-OUT       | VDD-CORE(1V1)                      |
| 36       | VCC-DRAM   (U7-OUT)  | VCC-DRAM(2V5)                      |
| 37       | -->R77(1K)-->U8-Pin4 | 显示背光，高电平打开背光，可PWM    |
| 38       | -->D1-->J1-6         | 低电平触发晃动报警，无晃动开关无效 |
| 39       | -->D21-->J1-4        | 外接电源指示                       |
| 40       | -->D22-->J1-3        | 未知功能                           |
| 41       | -->R20(1K)-->U14-Pin | 与Air202通信                       |
| 42       | -->R21(1K)-->U14-Pin | 与Air202通信                       |
| 43       | -->10K-->Q4-B        | 静音，低电平有效                   |
| 44       | -->R9(1K)-->U15-Pin1 | 高电平启动U15输出，为Air202供电    |

### PIN 45~66:

| 引脚编号 | 连接                                    | 可能的功能                           |
| -------- | --------------------------------------- | ------------------------------------ |
| 45       | J10-Pin9  &  -->R19(46K)3V3             | TF插入检测，插入后被接地             |
| 46       | -->R15(1K)-->Q1-B                       | 此处为高电平时通过Q1和Q8置J1-5高电平 |
| 47       | -->R108-->Q9-B                          | NC，RQ皆空焊盘，Q9-C连接到Air202     |
| 48       | -->SW2-->GND                            | SW2，按下低电平                      |
| 49       | U13-Pin2                                | 与U13的I2C通信的SDA，原机可能做加密  |
| 50       | VCC-IO                                  | VCC-IO(3V3)                          |
| 51       | HOSCI                                   | Crystal Input                        |
| 52       | HOSCO                                   | Crystal Output                       |
| 53       | U13-Pin4  & -->10K-->3V3                | 与U13的I2C通信的SCL，原机可能做加密  |
| 54       | 背面对应测试点                          | NC，原机做串口TXD，输出日志信息      |
| 55       | J10-Pin3  &  -->R47(10K)-->3V3          | TF卡槽的CMD                          |
| 56       | -->R49(33Ω)-->J10-Pin5                  | TF卡槽的CLK                          |
| 57       | J10-Pin7                                | TF卡槽的DAT0                         |
| 58       | U9附近测试点                            | NC，原机功能未测试                   |
| 59       | U9-Pin6                                 | 连接SPI Flash 的SCLK                 |
| 60       | U9-Pin1                                 | 连接SPI Flash 的CS#                  |
| 61       | U9-Pin2                                 | 连接SPI Flash 的SO                   |
| 62       | U9-Pin5                                 | 连接SPI Flash 的SI                   |
| 63       | -->R33(0Ω)-->U23-Pin*                   | UART,与RTL8710AF通信                 |
| 64       | -->R34(0Ω)-->U23-Pin*                   | UART,与RTL8710AF通信                 |
| 65       | U9与J10之间测试点                       | NC，原机功能未测试                   |
| 66       | -->R26(0Ω)--> [U23-Pin24--R30(10K上拉)] | 待研究                               |

### PIN 67~88:

| 引脚编号 | 连接                | 可能的功能                        |
| -------- | ------------------- | --------------------------------- |
| 67       | UVCC                | UVCC(3V3)                         |
| 68       | （背面测试点）      | USB   D-                          |
| 69       | （背面测试点）      | USB   D+                          |
| 70       | RESET               | /Reset                            |
| 71       | -->L1-->U4-OUT      | VDD-CORE(1V1)                     |
| 72       | NC                  | NC，手册中TVOUT                   |
| 73       | 3V3                 | TV-AVCC，TV电源                   |
| 74       | GND                 | TV-AGND，TV地                     |
| 75       | NC                  | NC，TV相关功能                    |
| 76       | NC                  | NC，TV相关功能                    |
| 77       | NC                  | NC，TV相关功能                    |
| 78       | NC                  | NC，TV相关功能                    |
| 79       | J1-Pin7             | 2/5 电池电压，IC厂商功能为ADC按键 |
| 80       | 3V3                 | AVCC，模拟信号部分的电源          |
| 81       | -->C19-->GND        | VRA1,Reference Voltage            |
| 82       | GND                 | AGND，模拟信号地                  |
| 83       | C18、R5、C20]-->GND | VRA2,Reference Voltage            |
| 84       | NC                  | IC厂商功能：FM in Right           |
| 85       | NC                  | IC厂商功能：FM in Left            |
| 86       | NC                  | IC厂商功能：LINL（Line IN）       |
| 87       | NC                  | IC厂商功能：Mic IN                |
| 88       | -->C76-->R59 ...    | Headphone-R OUT                   |







[Lexsion](https://lexsion.com)