---
layout: post
title: ESP8266 Reset EEPROM
---

Tool yang di gunakan adalah esptool petunjuk instalasi dapat dilihat di [https://github.com/espressif/esptool](https://github.com/espressif/esptool)

Langkah pertama check informasi board dengan  mengunakan command 

```esptool --port {portserial} flash_id```

![_config.yml]({{ site.baseurl }}/images/esp8266/esptool_flashid.png)

Dari info di atas didapatoi informasi flash size yang akan kita clearkan, 
untuk contoh di atas di dapatkan flash size sebesar 4MB.

Untuk mengClearkan flash dapat load file  (blank_1MB.bin)[files/blank_1MB.zip] kedalam flash tersebut 
dengan menggunakan command sebagai berikut 

```esptool --port  {portserial}  -b 115200 {address} blank_1MB.bin ```

Dalam contoh ini flash size nya adalah 4MB maka akan diload kedalam flash tersebut dengan command sebagai berikut 

![_config.yml]({{ site.baseurl }}/images/esp8266/esptool_write_blank.png)