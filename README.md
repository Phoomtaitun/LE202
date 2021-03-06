# สวัสดีครับทุกคน ผมนายภูมิไท ยินดี รหัสนักศึกษา 6310680365 ครับ
ก็ในวันนี้เราจะมาสรุปหัวข้อเรื่องต่าง ๆ กันนะครับโดยผมจะเรียบเรียงหัวข้อ และเนื้อหาที่น่าสนใจดังต่อไปนี้ครับ

# MARKDOWN
เราสามารถเขียนตัวหนา เอียง ได้จากการกดคีย์ลัดคล้าย ๆ MS WORD 
e.g. **Bold** -> cmd+B 
หรือ _ตัวเอียง_ -> cmd+i
อีกทั้งเรายังสามารถเน้นคำจากการเขียนเครื่องหมายมากกว่า (>)
>ทดสอบครับ
เราสามารถแทรกอิโมจิได้เช่น 🥺
เราสามารถสร้าง bullet point แบบ MS WORD 
ได้ด้วยเครื่องหมายขีดตรง (-) หรือตัวเลข 1. 2. 3.
- เป็น bullet point แบบนี้ได้เลย
- โดยถ้าเราเปิดการแก้ไข code จะเห็นเป็นขีดครับ
หรือเรายังสามารถกดเครื่องหมาย # เพื่อให้เป็นการขึ้นหัวข้อใหม่ โดยจะมีลักษณะ
ของตัวอักษรที่ใหญ่และดูน่าสนใจมากยิ่งขึ้นครับ
ยิ่งไปกว่านั้เรายังสามารถแทรกรูปภาพได้ด้วยนะครับ
![IMG_4594](https://user-images.githubusercontent.com/88340264/152791837-c7247d4e-ff0d-494d-b332-55f945597e62.jpg)


# สรุปเนื้อหาเกี่ยวกับ Microcontroller ESP-01
- digital ข้อมูล digital เกิดจากสัญญาณไฟฟ้ามาแทนด้วยเลขฐาน 2 มีแค่ 0, 1 จะขึ้นอยู่กับแรงดัน 
  หรือจะสามารถนำไปแสดงตัวอักษรแบบในรายวิชา LE242 ได้
- voltage คือความต่างศักย์ระหว่างจุดสองจุด มี 2 ประเภทคือ กระแสสลับ (AC) และ กระแสตรง (DC) ยกตัวอย่างเช่น battery และอุปกรณ์อื่น ๆ
- computor เป็นอุปกรณ์ช่วยใจการคำนวนทางคณิตศาสตร์และการกำหนดชุดคำสั่งต่าง ๆ
- internet สัญญาณที่เชื่อมอุปกรณ์ต่าง ๆ
- program lang การนำเอาภาษาที่ใช้สำหรับคอมพิวเตอร์มาสร้างเพื่อที่จะนำมาพัฒนา เพื่อให้คอมพิวเตอร์ช่วยคำนวน 
- platformio เป็นการพัฒนาซอฟแวร์แบบเปิด โดยเขียนลงบน microcontroller ได้หลากหลายแบบ เช่นเขียนแบบ Arduino และมี Libraies เสริมนำมาช่วยได้

# สรุปการทดลองบน ESP-01 จำนวน 6 การทดลอง
## ตัวอย่างที่ 1
โดยการทดลองจะเริ่มการเขียนโปรแกรมเข้าไปใน microcontroller และจะเริ่มนำเอาโปรแกรมเข้าไป
โดยจะมี 2 ส่วนจะมี setup และ loop และจะ loop หน่วงเวลา 1 sec โดยจะใช้ platformio และ upload program ลงไปใน microcontroller โดยจะต้องกดปุ่มด้วย แล้วกด pio device monitor จะเห็นได้ว่า count จะเพิ่มทีละ 1 ทุก ๆ 1 วินาที

## ตัวอย่างที่ 2 
เมื่อเสียบแล้วอัพโหลดโปรแกรมแล้ว จะมีส่วน setup (set wifi) แล้วเมื่อเจอแล้วจะแสดงผล เมื่ออัพโหลดโปรแกรมแล้วจะเริ่มสแกนหาโดยกด pio device monitor จะแสดงผล wifi ที่เจอ

## ตัวอย่างที่ 3 
จะมี output port และ input port แล้วเมื่อเสียบ USB แล้วจะมีช่องเสียบ computer ได้ เมื่อเสียบขอ io 0 แล้วเมื่อนำเอาโปรแกรมตัวอย่าง 3 จะทำให้ pin 0 เป็น output และจะวน loop every 0.5 sec และเพิ่มจำนวนรอบถ้าเป็นเลขคี่ให้เป็น on ส่วนคู่เป็น off และ LED จะส่องเมื่อเป็น ON

## Relay
จะนำเอา microcontroller ไปเสียบที่ relay เพื่อเอาไว้เปิดและปิด switch โดยจะทำให้เปิดปิดอุปกรณ์ได้

## ตัวอย่างที่ 4
โปรแกรม set ให้ port 0 เป็น input และ 2 เป็น output และโปรแกรมจะวน loop โดยอ่านข้อมูลจาก port 0 และถ้าเป็น 1 จะส่งไปยัง port 2 ให้เป็น off กล่าวคือสัญญาณ input port 0 เพื่อนำมาควบคุม output 
ถ้ามี voltage เข้าไปจะทำให้หลอด LED สว่างขึ้น

## ตัวอย่าง 5 
โปรแกรม wifi และใส่ชื่อและ password ลงไป โดย setup ระบุให้เชื่อม wifi เราจะทดสอบจากการเข้า web browser 

## ตัวอย่าง 6 
โปรแกรมใช้ wifi โดยจะสร้าง wifi ที่ต่อจาก mobile phone ได้ โดยมีการตั้งชื่อและมีการปล่อย wifi ให้คนมา connect โดยต้องกำหนด gate way และเตีรม websever โดยกำหนด password และ IP ลงไปเมื่ออัพโหลดโปรแกรม แล้วเมื่อ run จะปล่อย wifi ออกมา ยิ่งไปกว่านั้นเราจะทำการทดสอบโดยการนำเอาโทรศัพท์แล้วค้นหา wifi เมื่อพบแล้วเราสามารถเชื่อมต่อ wifi ได้
