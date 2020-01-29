##MQ135
=====

With this library you can obtain ppm for every MQ135 detectable gases

The way is simple, only imports the library to your .ino source code
> ```#include <MQ135.h>```

Instantiate the object 
>```MQ135 mqSensor(A0);/*Where A0 is the analogic input pin 0 where the output(analogic) of the sensor is A0*/```

No need to calibrate, it's done when it's booting but you should have good values after a reboot and 48h

Get the resistance (in void loop method)

> ```float resistance = mqSensor.getResistance();//resistance```

Get the gas reading
> ```float co = mqSensor.getCO(resistance);//co ppm&NewLine;float co2 = mqSensor.getCO2(resistance);//co2 ppm&NewLine;float ethanol = mqSensor.getEthanol(resistance);//ethanol ppm&NewLine;float nh4 = mqSensor.getNH4(resistance); //NH4 ppm&NewLine;float toluene = mqSensor.getToluene(resistance); //toluene ppm&NewLine;float acetone = mqSensor.getAcetone(resistance); //acetone ppm&NewLine;
  ```
