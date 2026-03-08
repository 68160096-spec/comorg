# Chapter 5: Internal Memory

สรุปเนื้อหาโครงสร้างและเทคโนโลยีของหน่วยความจำภายในคอมพิวเตอร์

## 5.1 Semiconductor Main Memory (หน่วยความจำหลักแบบเซมิคอนดักเตอร์)
* [cite_start]**Organization (การจัดองค์กร):** * องค์ประกอบพื้นฐานคือ **Memory Cell** ซึ่งมีคุณสมบัติแสดงสถานะเสถียรได้ 2 สถานะ (0 และ 1), สามารถเขียนข้อมูลลงไปได้ และสามารถอ่านข้อมูลออกมาได้
* **DRAM and SRAM (แรมแบบไดนามิกและสแตติก):**
    * [cite_start]**DRAM (Dynamic RAM):** เก็บข้อมูลในรูปของประจุไฟฟ้าในตัวเก็บประจุ (Capacitors) ต้องมีการ **Refresh** ข้อมูลเป็นระยะเพราะประจุจะรั่วไหล 
    * [cite_start]**SRAM (Static RAM):** ใช้การจัดรูปแบบลอจิกเกต (Flip-flop) เพื่อเก็บข้อมูล จะรักษาข้อมูลไว้ได้ตลอดตราบเท่าที่มีไฟเลี้ยง ไม่ต้องรีเฟรช และมีความเร็วสูงกว่า DRAM 
* **Types of ROM (ประเภทของรอม):**
    * [cite_start]**ROM:** ข้อมูลถูกเขียนถาวรระหว่างขั้นตอนการผลิต 
    * [cite_start]**PROM (Programmable ROM):** เขียนข้อมูลได้เพียงครั้งเดียวด้วยอุปกรณ์พิเศษ 
    * [cite_start]**EPROM:** ลบข้อมูลได้ด้วยแสง UV และเขียนใหม่ได้ 
    * [cite_start]**EEPROM:** ลบและเขียนใหม่ได้ด้วยสัญญาณไฟฟ้าในระดับ Byte 
* [cite_start]**Chip Logic & Packaging:** การจัดระดับสัญญาณผ่าน Address lines, Data lines และการใช้สัญญาณควบคุมเช่น RAS (Row Address Select) และ CAS (Column Address Select) เพื่อลดจำนวนขา (Pins) ของชิป 

## 5.2 Error Correction (การแก้ไขข้อผิดพลาด)
* **ประเภทความเสียหาย:** แบ่งเป็น **Hard Failure** (ความเสียหายถาวรที่ตัวฮาร์ดแวร์) และ **Soft Error** (ความผิดพลาดชั่วคราวจากสัญญาณรบกวน)
* **Hamming Code:** กลไกการใช้ Check bits เพื่อตรวจจับและแก้ไขข้อผิดพลาด
    * [cite_start]**SEC (Single-Error-Correcting):** แก้ไขข้อผิดพลาดได้ 1 บิต 
    * [cite_start]**SEC-DED:** แก้ไขได้ 1 บิต และตรวจจับได้ว่าผิดพลาด 2 บิต

## 5.3 DDR DRAM (แรมแบบ DDR)
* [cite_start]**SDRAM (Synchronous DRAM):** ทำงานสัมพันธ์กับสัญญาณนาฬิกา (Clock) ของระบบ ทำให้ Processor ไม่ต้องรอข้อมูลนานเกินไป
* [cite_start]**DDR (Double Data Rate):** * เพิ่มความเร็วในการส่งข้อมูลโดยส่งทั้งช่วง **ขาขึ้น (Rising edge)** และ **ขาลง (Falling edge)** ของสัญญาณนาฬิกา
    * [cite_start]มีการพัฒนาตั้งแต่ DDR1 จนถึง DDR4 โดยเพิ่มขนาด **Prefetch Buffer** และลดระดับแรงดันไฟฟ้าลง 

## 5.4 Flash Memory (หน่วยความจำแฟลช)
* [cite_start]**คุณสมบัติ:** เป็นหน่วยความจำแบบ Non-volatile (ข้อมูลไม่หายเมื่อไม่มีไฟ) ที่อยู่กึ่งกลางระหว่าง EPROM และ EEPROM ในด้านราคาและการทำงาน 
* **ประเภทของ Flash:**
    * **NOR Flash:** รองรับการเข้าถึงข้อมูลแบบสุ่ม (Random access) เหมาะสำหรับเก็บ Program Code
    * [cite_start]**NAND Flash:** มีความหนาแน่นข้อมูลสูงกว่า ลบและเขียนเป็นบล็อก (Block-level) เหมาะสำหรับที่เก็บข้อมูลความจุสูง

## 5.5 Newer Nonvolatile Solid-State Memory Technologies
เทคโนโลยีใหม่ที่พยายามรวมความเร็วของ RAM และความถาวรของ ROM เข้าด้วยกัน:
* **STT-RAM (Spin-Transfer Torque RAM):** ใช้ทิศทางการหมุนของอิเล็กตรอนในการเก็บข้อมูล
* **PCRAM (Phase-Change RAM):** ใช้การเปลี่ยนสถานะของวัสดุระหว่างผลึกและอสัณฐาน
* [cite_start]**ReRAM (Resistive RAM):** ใช้การเปลี่ยนความต้านทานไฟฟ้าของวัสดุฉนวน 

## 5.6 Key Terms, Review Questions, and Problems
* [cite_start]ส่วนสรุปคำศัพท์สำคัญ คำถามทบทวนเนื้อหา และแบบฝึกหัดท้ายบทเพื่อทดสอบความเข้าใจเกี่ยวกับการคำนวณ Check bits และการทำงานของหน่วยความจำ 
