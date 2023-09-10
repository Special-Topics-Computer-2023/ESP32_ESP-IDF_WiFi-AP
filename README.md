# ใบงานการสร้าง Wi-Fi Access Point (AP) ด้วย ESP-IDF

ในใบงานนี้ เราจะเรียนรู้การสร้าง Wi-Fi Access Point (AP) ด้วย ESP-IDF ซึ่งบอร์ด ESP32 ที่ใช้ในการทดลองมีความสามารถทั้งการเชื่อมต่อ WiFi ในฐานะอุปกรณ์ (station) และจุดกระจายสัญญาณ WiFi (Access point) 

## Access Point (AP) Introduction
Soft-Access point หรือ AP mode ของ ESP32 หมายถึง  “software-enabled access point.”  ที่ทำหน้าที่คล้าย ๆ  ‘virtual router,’
ที่ถูกสร้างจาก software ทำให้บอร์ด ESP32 ทำหน้าที่เป็น wireless access point

เมื่อ ESP32 ทำหน้าที่เป็น Soft-Access point มันจพสามารถสร้างเครื่อข่าย Wi-Fi ของตัวเอง และทำหน้าที่เป็น hot spot ให้ ESP32 ตัวอื่นหรือแม้กระทั่งคอมพิวเตอร์หรือ smartphone ได้


![](./ESP32_AP.png)

