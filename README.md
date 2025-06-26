# ☄️ Gemini

## 🌟 ภาพรวมของโครงการ

โครงการนี้เป็นการพัฒนาระบบซอฟต์แวร์สำหรับการควบคุมและจัดการกล้องโทรทรรศน์ Gemini โดยมีการออกแบบและพัฒนาตามมาตรฐาน Software Requirements Specification ที่กำหนดไว้ ระบบนี้ถูกสร้างขึ้นเพื่อรองรับการทำงานของผู้ใช้งานหลายประเภทในการดำเนินการทางดาราศาสตร์


![image](https://github.com/user-attachments/assets/717babec-c95d-4dee-847f-12b2a1267f7d)

## 👨🏻‍💼👩🏻‍💼 ประเภทของผู้ใช้งานภายในระบบ

ผู้ใช้งานระบบ Gemini จำแนกออกเป็น 5 ประเภท:

### A. Astronomer (นักดาราศาสตร์)
- ผู้ใช้ระบบ Gemini เพื่อเก็บรวบรวมข้อมูลทางวิทยาศาสตร์
- เป็นลูกค้าหลักของบริการที่ให้โดยกล้องโทรทรรศน์ Gemini
- ทำงานร่วมกับระบบ Gemini เพื่อจัดทำแผนงานวิทยาศาสตร์สำหรับการเก็บรวบรวมข้อมูล

### B. Science Observer (ผู้สังเกตการณ์ทางวิทยาศาสตร์)
- รับผิดชอบในการติดตามการเก็บรวบรวมข้อมูลและตรวจสอบความถูกต้องของข้อมูล
- ดูแลให้แผนงานวิทยาศาสตร์ทำงานตามความต้องการของนักดาราศาสตร์

### C. Telescope Operator (ผู้ควบคุมกล้องโทรทรรศน์)
- ควบคุมกล้องโทรทรรศน์และเครื่องมือต่างๆ ณ หน้างาน
- รับผิดชอบความสมบูรณ์ของระบบและการทำงานที่แม่นยำระหว่างการสังเกตการณ์
- ทำงานร่วมกับ Observer และแผนงานวิทยาศาสตร์เพื่อผลิตข้อมูลที่ดีที่สุด

### D. Support (ฝ่ายสนับสนุน)
- รับผิดชอบการบำรุงรักษาระบบทั้งฮาร์ดแวร์และซอฟต์แวร์
- ติดตั้งระบบย่อยและเปลี่ยนแปลงการกำหนดค่า

### E. Developer (นักพัฒนา)
- รับผิดชอบการออกแบบ, ทดสอบ, กำหนดค่า และอัพเกรดระบบย่อยต่างๆ

## 📌 Use Cases หลัก

โครงการนี้ประกอบด้วย 3 Use Cases หลัก:

### 1. Create Science Plan
- **Stakeholders and Interests**: Astronomers
- **Objective**: สร้างแผนงานวิทยาศาสตร์ (Science Plan)
- **Description**: กระบวนการสร้าง Science Plan ของนักดาราศาสตร์เพื่อวางแผนการสังเกตการณ์

### 2. Test Science Plan
- **Stakeholders and Interests**: Astronomers
- **Objective**: ทดสอบแผนงานวิทยาศาสตร์
- **Description**: กระบวนการทดสอบ Science Plan หลังจากที่มีการสร้างแผนงานเสร็จสิ้นแล้ว

### 3. Create Observing Program
- **Stakeholders and Interests**: Science Observer
- **Objective**: สร้างโปรแกรมการสังเกตการณ์
- **Description**: กระบวนการสร้าง Observing Program หลังจากที่ได้ validate Science Plan แล้ว เพื่อส่งให้ Operation Staff อนุมัติต่อไป

## 📋 เอกสารการออกแบบ

โครงการนี้รวมถึงเอกสารการออกแบบดังนี้:
- Use Case Diagrams
- Activity Diagrams
- Sequence Diagrams
- Use Case Descriptions
- Class Diagrams

# 🏃🏻‍♀️ วิธีการ run Project 🏃🏻‍♀️
1. เปิด cmd และใช้คำสั่ง `git clone` เพื่อ clone project ลงบนเครื่อง
2. เปิดโปรเจคใน IntelliJ IDEA และรัน build
3. ทำการสร้าง schema ใน MySQL ชื่อ `backend-ocs`
4. สร้างผู้ใช้ใน MySQL ด้วยข้อมูลต่อไปนี้:
   - Username: ceylon
   - Password: lowsweet
   - Host: localhost
   - Schema: backend-ocs
   - กำหนดสิทธิ์ให้ผู้ใช้สามารถเข้าถึง schema นี้ได้ (Select All)
5. รัน `DemoApplication` ใน IntelliJ IDEA
6. เปิดเว็บไซต์ที่ http://localhost:8080/
7. เข้าสู่ระบบโดยใช้อีเมลและรหัสผ่านตามข้อมูลด้านล่าง:

  🌅 **Astronomer:** 
   - Email: bai.tul@example.com, Password: baiCeylon
   - Email: tong.nit@example.com, Password: tongCeylon

  🌌 **SciObserver:**  
   - Email: pim.hah@example.com, Password: pimCeylon
   - Email: nai.nue@example.com, Password: naiCeylon
   - Email: my.san@example.com, Password: myCeylon

# 🦩 ขั้นตอนสร้างและทดสอบ SciPlan 🦩

1. เมื่อเข้าสู่ระบบด้วยบัญชีของ Astronomer คุณจะเห็นตาราง SciPlan ที่มี SciPlan ที่ถูกสร้างและทดสอบไว้แล้วของผู้ใช้ที่เข้าสู่ระบบ 
2. สามารถสร้าง SciPlan โดยกดปุ่ม `Create SciPlan` และกรอกข้อมูลที่ต้องการในหน้าต่างที่ pop-up ขึ้นมา
3. เมื่อกรอกข้อมูลเสร็จสิ้น ให้กดปุ่ม `Create` และตามด้วย `OK` เมื่อแจ้งเตือนแสดงขึ้นว่า Sciplan ได้ถูกสร้างเวร็จแล้ว
4. SciPlan ที่สร้างจะแสดงในตาราง SciPlan ที่ผู้ใช้ได้สร้างไว้
5. คุณสามารถทดสอบ SciPlan โดยกดปุ่ม `Test` ที่อยู่ในคอลัมน์สุดท้ายของแต่ละ SciPlan
6. เมื่อกด test SciPlan แล้วให้รอสักครู่ ผลลัพธ์จากการ test แสดงขึ้นว่า SciPlan นั้นผ่านการ test หรือไม่
7. เมื่อทดสอบเสร็จสิ้น สถานะของ SciPlan จะเปลี่ยนจาก `SAVED` เป็น `TESTED` และ SciPlan จะถูกย้ายไปยังตาราง SciPlan ที่ผ่านการทดสอบ

# 🦚 ขั้นตอนสร้าง Observing Program 🦚

1. เมื่อเข้าสู่ระบบด้วยบัญชีของ SciObserver คุณจะเห็นตาราง SciPlan ที่ถูกสร้างไว้และตรงส่วนด้านล่างของตารางจะมี Observing Program ที่เป็นช่องว่างๆไว้ (ต้องสร้าง Observing Program ก่อนถึงจะเห็น)
2. SciObserver สามารถสร้าง Observing Program ได้โดยกดปุ่มที่อยู่ในคอลัมน์สุดท้ายของแต่ละ SciPlan
3. หลังจากกดปุ่ม `Create Observing Program` คุณจะได้แสดงหน้าต่างที่ pop-up เพื่อให้กรอกข้อมูล Observing Program
4. เมื่อกรอกข้อมูลเสร็จสิ้น ให้กดปุ่ม `Submit` และตามด้วย `OK` เมื่อแจ้งเตือนแสดงขึ้น
5. Observing Program ที่สร้างจะแสดงในช่องว่างด้านล่างตรงส่วนของ Observing Program


# 🧘🏻 Design Patterns 🧘🏻

**_Facade Pattern_**

เนื่องจากมีการเรียกใช้งานฟังก์ชันต่างๆ ทั้งการ fetchSciencePlans() และ fetchObservingPrograms() เพื่อดึง api มาแสดงผลในหน้าเว็บไซต์ ที่เป็นตัวกลางในการเชื่อมต่อในการเรียกใช้งานระบบย่อยอื่นๆ รวมถึงการเรียกใช้งาน method จาก OCS ด้วย ซึ่งการใช้ Facade Pattern ช่วยให้สามารถลดความซับซ้อนของระบบย่อยต่างๆ ไว้ภายในฟังก์ชันหลัก ทำให้การใช้งานระบบทั้งหมดมีความง่ายและสะดวกมากขึ้น

---

