# Unit OP 90 {docsify-ignore-all}

<img src="assets/img/product_pics/unit/op90/op90_01.jpg" width="30%" height="30%"><img src="assets/img/product_pics/unit/op90/aop90_02.jpg" width="30%" height="30%">

***

:memo:**[Description](#Description)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:octocat:**[Example](#Example)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; :electric_plug:**[Schematic](#Schematic)** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🛒**[Purchase](https://www.aliexpress.com/store/product/M5Stack-Official-ADC-Unit-16-Bit-I2C-GROVE-ADS1100-Module-0V-to-12V-analog-to-digital/3226069_32946953374.html?spm=a2g1x.12024536.productList_5885013.pic_7)**

## Description

OP.90 and OP.180 are two limit switches with different orientation placement.
<br>
They are used for controlling machinery as part of a control system, as a safety interlock, or to count objects passing a point.A limit switch is an electromechanical device that consists of an actuator mechanically linked to a set of contacts. When an object comes into contact with the actuator, the device operates the contacts to make or break an electrical connection
<br>
The actuator of this Unit is consist of a pair of IR part, emitter side and receiver side. The IR emitter will keep sending IR wave while the receiver will keep detecting the IR wave.  The IR is directly emitted from one side to another side, so if there's no object in between, the receiver side would get the IR signal. This is how it detecting a break an electrical connection. 



### Product Features

- Horizontal/vertical
- IR limit switch 

## Include

- 1x ADC unit
- 1x GROVE Cable
- 1x HT3.96 Male Socket(2 pins)

## Application

- Door switch
- machinery control 


## Dcumentation

  
## Schematic
<img src="assets/img/product_pics/unit/op90/op90_04.jpg">


## EasyLoader

<img src="https://m5stack.oss-cn-shenzhen.aliyuncs.com/image/EasyLoader_logo.png" width="100px" style="margin-top:20px">

<a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/EasyLoader/Unit/EasyLoader_ADC.exe"><button type="button" class="btn btn-primary">click to download EasyLoader</button></a>

>1.EasyLoader is a simple and fast program burner, and each product page has a product-related case program for EasyLoader.

>2.After downloading the software, double-click to run the application, connect the M5 device to the computer via the data cable, select the port parameters, and click **"Burn"** to start burning.

!>3.The CP210X (USB driver) needs to be installed before the EasyLoader is burned. [Click here to view the driver installation tutorial](en/related_documents/establish_serial_connection)

## Example

### 1. Arduino IDE

*The below code is incomplete(just for usage). If you want the complete code, please click [here](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/ADC/Arduino/ADC_ADS1100).*

```arduino
#include <M5Stack.h>
#include <Wire.h>
#include "ADS1100.h"

#define ADS1100_DEFAULT_ADDRESS 0x48

// declaration
byte error;
int8_t address;

//new a object
ADS1100 ads;

// initialization
M5.begin(true, false, false);
ads.getAddr_ADS1100(ADS1100_DEFAULT_ADDRESS);// 0x48, 1001 000 (ADDR = GND)
ads.setGain(GAIN_ONE);          // 1x gain(default)
ads.setMode(MODE_CONTIN);       // Continuous conversion mode (default)
ads.setRate(RATE_8);            // 8SPS (default)
ads.setOSMode(OSMODE_SINGLE);   // Set to start a single-conversion
ads.begin();

// read data
address = ads.ads_i2cAddress;
Wire.beginTransmission(address);
Wire.endTransmission();
ads.Measure_Differential();
```

### 2. UIFlow

*If you want the complete code, please click [here](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/ADC/UIFlow).*

<img src="assets/img/product_pics/unit/unit_example/ADC/example_unit_adc_01.png">