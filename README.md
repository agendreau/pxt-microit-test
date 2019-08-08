 # Challenge
Sound Sensor Data Collection Challenge

## Step 1
``||basic: Continuously||`` collect ``||gatorSound: sound||`` samples every two seconds and ``||radio: send||`` them 
to the data display application which is listening on radio channel 7. 
Do not forget to set your ``||radio: channel||`` to 7.
When you think, you've got it, download it and try it out.

```blocks
radio.setGroup(7)
basic.forever(function () {
    radio.sendNumber(gatorMicrophone.getSoundIntensity())
    radio.sendNumber(gatorEnvironment.getMeasurement(measurementType.degreesF))
    basic.pause(2000)
})
```




```package
gatorMicrophone=github:sparkfun/pxt-gator-microphone
gatorEnvironment=github:sparkfun/pxt-gator-environment
```


