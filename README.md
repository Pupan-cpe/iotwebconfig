# iotwebconfig
for ESP32
ไลบารี่สำหรับใช้แทน Wifimanager สำหรับ ESP32 โดยได้ทำการปรับปรุงให้สามารถรองรับกับ ESP32 ได้ 

#วิธีใช้ 
<br>1.คุณเปิด IoT ของคุณเป็นครั้งแรก - เปลี่ยนเป็นโหมด AP (จุดเข้าใช้งาน) และรอคุณอยู่ที่ 192.168.4.1 ที่อยู่พร้อมกับเว็บอินเตอร์เฟสเพื่อตั้งค่าเครือข่ายท้องถิ่นของคุณ (และการกำหนดค่าอื่น ๆ ) เป็นครั้งแรกที่ใช้รหัสผ่านเริ่มต้นเมื่อคุณเชื่อมต่อกับ AP เมื่อคุณเชื่อมต่อกับ AP อุปกรณ์ของคุณจะปรากฏขึ้นโดยอัตโนมัติในหน้าพอร์ทัล (เราเรียกสิ่งนี้ว่า Captive Portal) เมื่อการกำหนดค่าเสร็จสิ้นคุณต้องออกจาก AP อุปกรณ์ตรวจพบว่าไม่มีใครเชื่อมต่อและทำงานต่อตามปกติ<br>
<br>2.การกำหนดค่า WiFi มีการเปลี่ยนแปลงเช่นสิ่งถูกย้ายไปยังตำแหน่งอื่น - เมื่อสิ่งไม่สามารถเชื่อมต่อกับ WiFi ที่กำหนดค่าจะกลับไปที่โหมด AP และรอให้คุณเปลี่ยนการกำหนดค่าเครือข่าย เมื่อไม่มีการกำหนดค่าแล้วจะพยายามเชื่อมต่อกับการตั้งค่าที่กำหนดไว้แล้ว สิ่งที่จะไม่ปิด AP ในขณะที่ทุกคนเชื่อมต่อกับมันดังนั้นคุณต้องออกจาก AP เมื่อเสร็จสิ้นการกำหนดค่า<br>
<br>3.คุณต้องการเชื่อมต่อกับ AP แต่ลืมรหัสผ่าน AP WiFi ที่กำหนดค่าที่คุณตั้งไว้ก่อนหน้านี้ - เชื่อมต่อพินที่เหมาะสมบน Arduino ลงกราวด์ด้วยปุ่มกด กดปุ่มค้างไว้ในขณะที่เปิดเครื่องอุปกรณ์ทำให้สิ่งที่จะเริ่มโหมด AP ด้วยรหัสผ่านเริ่มต้น (ดูกรณีที่ 1 รหัสถูกกำหนดค่าในรหัส)<br>
คุณต้องการเปลี่ยนการกำหนดค่าก่อนที่สิ่งที่เชื่อมต่อกับอินเทอร์เน็ต - ดี! สิ่งที่เริ่มต้นขึ้นในโหมด AP เสมอและให้กรอบเวลาในการเชื่อมต่อและทำการปรับเปลี่ยนใด ๆ กับการกำหนดค่า ทุกครั้งที่เชื่อมต่อกับ AP (จัดหาโดยอุปกรณ์) AP จะยังคงเปิดอยู่จนกว่าการเชื่อมต่อจะปิด ดังนั้นใช้เวลาของคุณสำหรับการเปลี่ยนแปลงสิ่งที่จะรอคุณในขณะที่คุณเชื่อมต่อกับมัน
<br>4.คุณต้องการเปลี่ยนการกำหนดค่าที่รันไทม์ - ไม่มีปัญหา IotWebConf ช่วยให้พอร์ทัลการตั้งค่าสามารถทำงานได้แม้หลังจากการเชื่อมต่อ WiFi เสร็จสิ้นแล้ว ในสถานการณ์นี้คุณต้องป้อนชื่อผู้ใช้ "ผู้ดูแลระบบ" และรหัสผ่าน (กำหนดค่าแล้ว) เพื่อเข้าสู่พอร์ทัลปรับแต่ง โปรดทราบว่ารหัสผ่านที่ให้ไว้สำหรับการตรวจสอบความถูกต้องจะไม่ถูกซ่อนจากอุปกรณ์ที่เชื่อมต่อกับเครือข่าย WiFi เดียวกัน คุณอาจต้องการบังคับให้บูตเครื่องใหม่เพื่อใช้การเปลี่ยนแปลงของคุณ

#Credits
Although IotWebConf started without being influenced by any other solutions, in the final code you can find some segments borrowed from the WiFiManager library.<br>
https://github.com/prampec/IotWebConf <br>
https://github.com/tzapu/WiFiManager

Thanks to all contributors providing patches for the library!
