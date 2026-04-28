📊 Live Lab: Data Type Selection and Conversion
CompTIA Data+ (DA0-001) Implementation
📝 Project Overview (ภาพรวมโครงการ)
This project focuses on the foundational skills of a Data Analyst: ensuring data consistency and integrity across multiple platforms. In this lab, I performed end-to-end data type management—starting from the SQL source level to the transformation layer in Power Query.



โปรเจกต์นี้เน้นการฝึกฝนทักษะพื้นฐานที่สำคัญที่สุดของ Data Analyst คือการทำให้ข้อมูลมีความถูกต้องและสอดคล้องกันในทุกแพลตฟอร์ม โดยผมได้ดำเนินการจัดการประเภทข้อมูลตั้งแต่ระดับต้นทาง (SQL Database) ไปจนถึงขั้นตอนการแปลงข้อมูล (Transformation) ใน Power Query

<img width="1517" height="825" alt="1 4 11" src="https://github.com/user-attachments/assets/ffc9ecef-e0f6-4bdf-be13-555a1f12409c" />



🛠️ รายละเอียดสิ่งที่คุณได้ลงมือทำ (Implementation Details)
1.การสำรวจและออกแบบโครงสร้างต้นทาง (SQL Data Profiling & Design):
  คุณได้เข้าไปตรวจสอบโครงสร้างตาราง (Table Schema) ใน SQL Server เพื่อหาจุดที่ประเภทข้อมูลไม่เหมาะสม (Type Mismatches)
  ลงมือแก้ไขคุณสมบัติของ Field ผ่าน Design View เช่น การเปลี่ยนจากข้อความ (VARCHAR) ที่เก็บตัวเลข ให้กลายเป็นจำนวนเต็ม (INT) เพื่อลดขนาดการจัดเก็บและทำให้การประมวลผลคำสั่ง Query รวดเร็วขึ้น



2.การเชื่อมต่อและดึงข้อมูล (Database Connectivity):
  จัดการทำ Seamless Connection ระหว่างฐานข้อมูล SQL และเครื่องมือวิเคราะห์ เพื่อให้มั่นใจว่าข้อมูลไหลเข้าสู่ Pipeline ได้อย่างถูกต้อง 100%



3.กระบวนการ ETL และการทำ Data Casting:
  ใช้ Power Query เป็นเครื่องมือหลักในการทำความสะอาดข้อมูล
  ดำเนินการ Data Casting หรือการแปลงประเภทข้อมูลในขั้นตอนสุดท้าย เช่น การจัดการรูปแบบวัน/เวลา (Date/Time) และความละเอียดของจุดทศนิยม (Decimal Precision) เพื่อป้องกันการเกิด "Data Loss" หรือข้อมูลเพี้ยนระหว่างย้ายจากฐานข้อมูลมายังรายงาน




สรุปสิ่งที่ได้รับ:
ผลการประเมิน: ทำภารกิจสำเร็จครบถ้วน ได้คะแนนเต็ม
ความเชี่ยวชาญ: เข้าใจหลักการของ CompTIA Data+ ในเรื่องการระบุแหล่งที่มาและการดึงข้อมูล
ความแม่นยำ: สามารถแปลงข้อมูลได้โดยไม่มี Error หรือข้อมูลสูญหาย (Zero-Error)
ทักษะการวิเคราะห์: รู้วิธีการเลือกใช้ Data Type ให้เหมาะสมกับความต้องการของธุรกิจ
