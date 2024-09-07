# esp32
通过这一个项目可以实现一个带有氛围灯的esp32 Wifi 天气时钟, 这一个项目里面的教程包括PCB设计, 3D打印外壳的设计, 软件的设计

![成品图片](https://picture-01-1316374204.cos.ap-beijing.myqcloud.com/image/202409071137114.png)

[这一个是v1.0的的测试视频](https://www.bilibili.com/video/BV1RnYReXEdh/?spm_id_from=333.999.0.0), 目前这一个开发板的硬件还有一点bug(led的灯光不稳定), 目前猜测是电压问题或者信号干扰, 但是由于最近比较忙一直没有实际测试, 以后有时间会优化的

目前在测试Mqtt远程实现一个弹窗信息提示

其他的学习资料可以看一下这一个[嵌入式学习路线 (know-cnu.wiki)](https://embedded-study-guide.know-cnu.wiki/)

实际使用的是ESP-IDF v5.1.4

![image-20240907154425406](https://picture-01-1316374204.cos.ap-beijing.myqcloud.com/image/202409071544460.png)

使用自己的分区表

![image-20240907154504509](https://picture-01-1316374204.cos.ap-beijing.myqcloud.com/image/202409071545543.png)

lvgl使用QR库

```c
dependencies:
  espressif/esp_lcd_touch:
    component_hash: d4d8f2dc33205797169a97a02e0d89a8982f59fe0509129b54422052b8522f59
    source:
      storage_url: file:///E:/alearn/ESP-IDF-5_1_4/Espressif/registry
      type: service
    version: 1.1.1
  espressif/zlib:
    component_hash: 999ec50086ac1c82b8321d8f540dc9fd10f5622948b935558aa16b4b66e95d9d
    source:
      type: service
    version: 1.3.0
  espressif__esp_lcd_touch_ft5x06:
    component_hash: null
    source:
      path: E:\JHY\esp32\ESP-IDF\2024-8-3-jiao-ESP32\components\espressif__esp_lcd_touch_ft5x06
      type: local
    version: 1.0.6
  idf:
    component_hash: null
    source:
      type: idf
    version: 5.1.4
  lvgl/lvgl:
    component_hash: 948bff879a345149b83065535bbc4a026ce9f47498a22881e432a264b9098015
    source:
      storage_url: file:///E:/alearn/ESP-IDF-5_1_4/Espressif/registry
      type: service
    version: 8.3.11
manifest_hash: f8acd3c53fe97b7bd7f866e9e690cc329aa47d9190d9542797e4897a80c30134
target: esp32
version: 1.0.0
```

> 使用的组件和版本
