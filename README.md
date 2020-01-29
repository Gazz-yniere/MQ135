##MQ135
=====

With this library you can obtain ppm for every MQ135 detectable gases

The way is simple, only imports the library to your .ino source code
> ```#include <MQ135.h>```

Instantiate the object 
>```MQ135 mqSensor(A0);/*Where A0 is the analogic input pin 0 where the output(analogic) of the sensor is A0*/```

First you need the resistance zero, leave the sensor connected 24hrs outside and obtain it for each gas with this methods:
> ```
  float getRZeroCO();
  float getRZeroCO2();
  float getRZeroEthanol();
  float getRZeroNH4();
  float getRZeroToluene();
  float getRZeroAcetone();
```

Call them with 

>```
float resistanceZero = mqSensor.getRZeroCO();
```

Change the resistance zero in 

> MQ135/MQ135.h

Get the resistance (in void loop method)

> ```float resistance = mqSensor.getResistance();//resistance```

Get the gas reading
> ```
  float co = mqSensor.getCO(resistance);//co ppm
  float co2 = mqSensor.getCO2(resistance);//co2 ppm
  float ethanol = mqSensor.getEthanol(resistance);//ethanol ppm
  float nh4 = mqSensor.getNH4(resistance); //NH4 ppm
  float toluene = mqSensor.getToluene(resistance); //toluene ppm
  float acetone = mqSensor.getAcetone(resistance); //acetone ppm
```


