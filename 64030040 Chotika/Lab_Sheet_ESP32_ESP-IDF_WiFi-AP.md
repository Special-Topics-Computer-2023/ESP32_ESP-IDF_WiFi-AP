# ใบงานการทดลอง ESP32_ESP-IDF_WiFi-AP

## ขั้นตอนการทดลอง

1. สร้าง Espressif IDF project ใหม่ ชื่อ  ESP32_ESP-IDF_WiFi-AP 


1.1  หลังจากใส่ชื่อ คลิก next เพื่อเลือก template project

![Alt text](./Pictures/1.Create-new-project.png)


1.2 เลือก template project เป็น softAP

![Alt text](Pictures/2.Select-template.png)


### 2. แก้ไขไฟล์ config

2.1 เปิดไฟล์ Kconfig.projbuild  ในโฟลเดอร์ main ด้วย text editor


![Alt text](./Pictures/3.open-Kconfig-file.png)

[1] เปิด folder  main
 
[2] คลิกขวาที่ชื่อไฟล์ Kconfig.projbuild

[3] เลือก Open With
 
[4] เลือก Text Editor


2.2 แก้ไขไฟล์

![Alt text](./Pictures/4.Edit-Kconfig-file.png) 

[1] แก้ไข SSID  ให้มีความแตกต่างจากของเพื่อน โดยใส่เลข 3 ตัวท้ายของรหัสนักศึกษากำกับไว้ เช่น `"SSID-001"` เป็นต้น

[2]  อาจจะแก้ password ตามต้องการ

หมายเหตุ ไฟล์นี้สามารถแก้ได้ภายหลังจากการเรียก  sdkconfig

### 3. Build โปรเจค

### 4. Run โปรเจค ดูผลจาก Terminal

### 5. ใช้ Laptop หรือ Smartphone ค้นหา Accesspoint 

ควรจะต้องเจอ `"SSID-..."` ในรายการ Wifi ที่เราสร้างขึ้น

### 6. บันทึกผลการทดลอง 

ทั้งที่หน้าจอ Laptop หรือ Smartphone และที่ terminal ของ ESP32

รวมทั้งหน้าจอ properties ของ wifi ดังตัวอย่าง

![Alt text](./Pictures/5.Example_Wifi_Properties.png)
### 7. ส่งงาน

โดยการ pull request พร้อมแนบ link ไปยัง Repository ของโปรเจคมาด้วย

![Alt text](Pictures/Lab_AP_01.png)
![Alt text](Pictures/Lab_AP_02.png)

## Link Repository
https://github.com/CHOTIKA040/ESP32_ESP-IDF_WiFi-AP-