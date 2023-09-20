## อธิบาย
**ผมเชื่อว่าหลายคนในการเริ่มเรียนเกี่ยวกับ CyberSecurity ด้วยตัวเองอาจต้องเจอปัญหาในเรื่องนี้เนื่องจากขาดความรู้ ผมเองก็เคยเป็นแล้วหลายๆที่ให้ผมสอนก็เป็น**

## การโจมตีจริงเป็นแบบไหน
**การโจมตีจริงๆก็ไม่ได้ต่างกับที่เราทดลองเรียนรู้ในตอนเริ่มต้นมากนักแต่อาจมีข้อแตกต่างเล็กน้อยเช่น คุณอาจจะทำการโจมตีเว็บด้วยการใช้ Reverse Shell แต่พบว่าไม่สามารถทำได้**
* **1.คุณต้องมันใจก่อนว่า Sever นั้นใช้ Windows หรือ Linux (ส่วนมากเป็น Linux)**
* **2.คุณอาจต้องใช้ Ngrok เพื่อเชื่อมต่อกับเป้าหมาย หากคุณไม่ได้ใช้ WIFI เดียวกับ sever และหากคุณขี้เกียจตั้งค่า Router ของคุณเอง**
* **3.หากคุณใช้ Ngrok เวลาคุณจะให้เป้าหมายเชื่อมต่อกลับมาคุณจำเป็นต้องใช้ url และ port ของ Ngrok เช่น 0.tcp.ap.ngrok.io:16448 -> TCP**

## ตัวอย่างของ netcat –lvp 4444
```
tcp://0.tcp.ap.ngrok.io:16448 -> localhost:4444

tcp://0.tcp.ap.ngrok.io:16448 -> คือสิ่งที่เราจะใช้ให้ payload เชื่อมต่อกลับมา
localhost:4444 -> คือสิ่งที่ทำการเชื่อมต่อกับเป้าหมาย
```

## ตัวอย่างของ Metasploit 
![Screenshot 2023-09-20 224605](https://github.com/Thampakon/Fix-Learning-CyberSecurity/assets/119696243/91e0d6fc-2490-4639-9a9e-28fbf4024818)
