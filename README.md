# This is a try to make the ESP8266 OTA programming by Auto update form GitHub site.

>  # **Note:**
> 
> This Project has some errors which asked [here][1]:
> 
> [![enter image description here][2]][2]

### The main instruction:

First you need to do these steps:

1- the file made for the target codes as **version.txt** file with the Above amount (**2.0** here):

```
const String FirmwareVer={"2.0"};//{"1.8"};

```
you need to build this file via the Arduino target project at your GitHub repo as you can see below:
```
#define URL_fw_Version "https://github.com/soheilpaper/ota_github_blink/blob/main/version.txt"

```

![enter image description here](https://i.stack.imgur.com/lqGKs.png)


3- you need to create the .bin file of your Arduino project like shown below and upload the bin file to your GitHub project and give its  **URL_fw_Bin** as the target program to be updated automatically to Arduino board:

[![enter image description here][3]][3]


    #define URL_fw_Bin "https://github.com/soheilpaper/ota_github_blink/blob/main/BlinkWithoutDelay.ino.esp8285.bin" //"https://raw.githubusercontent.com/programmer131/otaFiles/master/firmware.bin"

4- Finally upload [the main code][4] (GitHub_OTA Codes) to Arduino as you can see below:

[![enter image description here][5]][5]

Also, you can test it by [this video][6]:

[**ESP8266 Self Update OTA from Github**][6]


[![enter image description here][7]][7]


##Other methods:

There are some other methods described here:

 1. [Over-The-Air(OTA) update for Arduino by AglowOTA][8]

[![enter image description here][9]][9]

 2. [Serverless Continuous Integration and OTA update flow for IoT
    devices using Google Cloud Build and Arduino][10]
[![enter image description here][11]][11]

Thanks for your attention.


  [1]: https://arduino.stackexchange.com/questions/80890/error-101-server-did-not-report-size-from-ota-upgrade-framework-via-git-hub
  [2]: https://i.stack.imgur.com/8r8sI.png
  [3]: https://i.stack.imgur.com/LwYE9.png
  [4]: https://github.com/soheilpaper/ota_github_blink/blob/main/ESP_OTA_Github.ino
  [5]: https://i.stack.imgur.com/z72Rc.png
  [6]: https://www.youtube.com/watch?v=FuY6BobS-1k&feature=youtu.be
  [7]: https://i.stack.imgur.com/rUttb.png
  [8]: https://medium.com/@aglowbytickle/over-the-air-ota-for-arduino-by-aglowota-205eac78e664
  [9]: https://i.stack.imgur.com/pROfj.png
  [10]: https://medium.com/google-cloud/serverless-continuous-integration-and-ota-update-flow-using-google-cloud-build-and-arduino-d5e1cda504bf
  [11]: https://i.stack.imgur.com/9uXUO.png


