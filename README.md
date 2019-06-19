## Project under construction :construction:

This project are curently (2019/06/18) under construction.

---

# EzoDeviceLib
UWP Library for Atlas Scientific EZO devices
Open source UWP library for communication with Atlas Scientific EZO devices. This library covers all I2C commands. You can trigger measurements, set temperature compensation, get device info and state, due the calibration, import/export calibration data, etc.

This library targets __UWP IoT projects__! Download directly from NuGet [Rca.EzoDeviceLib on NuGet](https://nuget.org/packages/Rca.EzoDeviceLib).

* Support for EZO devices


## How to use?
Some basic usage examples

### Create an sensor instance
In this example is the I2C address of conneted EZO device set to default (0x63 for EZO pH Circuit):

```cs
var myEzoPhSensor = new PhSensor();
```

Or create an instance with custom parameters:

```cs
var myEzoPhSensor = new PhSensor(0x1A)
{
	BusSpeed = I2cBusSpeed.FastMode //default is StandardMode
};
```

	
### Perform an read measurement
	
```cs
double ph = myEzoPhSensor.GetMeasValue();
```

With tempreature compensation:

```cs
double temperature = 23.5; //temperature in °C
double phCompensated = myEzoPhSensor.GetMeasValue(temperature);
```


## How To install?
Download the source from GitHub or get the compiled assembly from NuGet [Rca.EzoDeviceLib on NuGet](https://nuget.org/packages/Rca.EzoDeviceLib).

## Credits
This library is made possible by contributions from:
* [Elias Rümmler](http://www.100prznt.de) ([@rmmlr](https://github.com/rmmlr)) - core contributor

## License

Rca.EzoDeviceLib is licensed under [MIT](http://www.opensource.org/licenses/mit-license.php "Read more about the MIT license form"). Refer to [license.txt](https://github.com/100prznt/EzoDeviceLib/blob/master/LICENSE) for more information.

## Contributions

Contributions are welcome. Fork this repository and send a pull request if you have something useful to add.

Build status...


## Related Projects

* [OpenPoolControl](https://github.com/100prznt/opc)
