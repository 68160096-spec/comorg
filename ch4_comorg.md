# Chapter 4: Cache Memory

## 4.1 Computer Memory System Overview

Computer memory มีหลายประเภท ทั้งด้าน **technology, organization, performance และ cost**  
ดังนั้นระบบคอมพิวเตอร์จึงใช้ **Memory Hierarchy** เพื่อให้ได้ทั้งความเร็วและความจุที่เหมาะสม

---

### Characteristics of Memory Systems

หน่วยความจำสามารถจำแนกตามคุณลักษณะหลักดังนี้

#### 1. Location
- **Internal Memory**
  - Registers
  - Cache
  - Main Memory
- **External Memory**
  - Hard disk
  - Optical disk
  - Magnetic tape

#### 2. Capacity
- จำนวน **Words**
- จำนวน **Bytes**

#### 3. Unit of Transfer
- **Word**
- **Block**

#### 4. Access Method
- **Sequential Access**  
  เข้าถึงข้อมูลตามลำดับ (เช่น Tape)

- **Direct Access**  
  เข้าถึง block ที่ต้องการได้โดยตรง แต่เวลาไม่คงที่ (เช่น Disk)

- **Random Access**  
  เข้าถึงตำแหน่งใดก็ได้ในเวลาเท่ากัน (เช่น RAM)

- **Associative Access**  
  ค้นหาข้อมูลจาก **content** แทน address

---

### Memory Performance

ตัวชี้วัดหลักของประสิทธิภาพหน่วยความจำ

- **Access Time (Latency)**  
  เวลาที่ใช้ในการอ่านหรือเขียนข้อมูล

- **Memory Cycle Time**  
  เวลาในการทำ operation หนึ่งครั้ง + เวลาที่ต้องรอก่อนทำครั้งถัดไป

- **Transfer Rate**  
  อัตราการถ่ายโอนข้อมูล

