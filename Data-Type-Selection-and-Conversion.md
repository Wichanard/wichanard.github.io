#  📊 Live Lab: Data Type Selection and Conversion
CompTIA Data+ (DA0-001) Implementation
📝 Project Overview (ภาพรวมโครงการ)
This project focuses on the foundational skills of a Data Analyst: ensuring data consistency and integrity across multiple platforms. In this lab, I performed end-to-end data type management—starting from the SQL source level to the transformation layer in Power Query.



# โปรเจกต์นี้เน้นการฝึกฝนทักษะพื้นฐานที่สำคัญที่สุดของ Data Analyst คือการทำให้ข้อมูลมีความถูกต้องและสอดคล้องกันในทุกแพลตฟอร์ม โดยผมได้ดำเนินการจัดการประเภทข้อมูลตั้งแต่ระดับต้นทาง (SQL Database) ไปจนถึงขั้นตอนการแปลงข้อมูล (Transformation) ใน Power Query

# โดยมีขั้นตอนดังนี้

# ภาพที่ 1: การเช็คแหล่งข้อมูล (Data Source Exploration)
<img width="842" height="840" alt="1 1" src="https://github.com/user-attachments/assets/ecd7c4d3-5309-462b-9a09-ea4fde3109fe" />
สิ่งที่กำลังทำอยู่: เรากำลังใช้งาน Microsoft SQL Server Management Studio (SSMS) เพื่อสำรวจฐานข้อมูล TDHS_StudentInfoSys
รายละเอียด: คลิกขวาที่ตาราง dbo.tblEnrollment และเตรียมใช้คำสั่ง Select Top 1000 Rows นี่คือขั้นตอนแรกในการทำ Data Profiling เพื่อขอดูหน้าตาข้อมูลคร่าวๆ ว่ามีลักษณะอย่างไรก่อนนำไปดึงไปประมวลผลต่อ



# ภาพที่ 2: การตรวจสอบโครงสร้างข้อมูล (Schema & Data Type Inspection)
<img width="467" height="247" alt="1 2" src="https://github.com/user-attachments/assets/004c0198-76fc-4443-9583-d94a53573126" />
สิ่งที่กำลังทำอยู่: เปิดดูหน้าต่าง Design ของตาราง dbo.tblEnrollment เพื่อตรวจสอบ Data Dictionary หรือ Schema ของตารางนี้
รายละเอียด: ระบบแสดงให้เห็นชื่อคอลัมน์และ Data Type ต้นทางอย่างชัดเจน เช่น EnrollmentID เก็บเป็น int (ตัวเลขจำนวนเต็ม), EnrollmentDate เป็น datetime (วันและเวลา) และ SchYr_Grade เป็น nvarchar(2) (ข้อความ) การรู้ว่าระบบฐานข้อมูลต้นทางเก็บข้อมูลมาแบบไหน จะช่วยให้เราวางแผนแปลงข้อมูลได้อย่างถูกต้อง



# ภาพที่ 3: การแปลงประเภทข้อมูล (Data Type Conversion)
<img width="960" height="852" alt="1 3" src="https://github.com/user-attachments/assets/b5e91fec-4508-4ef9-a521-d613e080d773" />
สิ่งที่กำลังทำอยู่: ข้อมูลถูกดึงเข้ามาใน Power Query Editor เพื่อทำการแปลงข้อมูล (Data Transformation)
รายละเอียด: คุณกำลังคลิกเมนู Dropdown ที่หัวคอลัมน์ EnrollmentID เพื่อเปลี่ยนประเภทข้อมูล (Change Type) โดยกำลังจะเปลี่ยนจากตัวเลขให้กลายเป็น Text (ข้อความ)



# 🛠️ รายละเอียดสิ่งที่ได้ลงมือทำ (Implementation Details)
1.การสำรวจและออกแบบโครงสร้างต้นทาง (SQL Data Profiling & Design):
  คุณได้เข้าไปตรวจสอบโครงสร้างตาราง (Table Schema) ใน SQL Server เพื่อหาจุดที่ประเภทข้อมูลไม่เหมาะสม (Type Mismatches)
  ลงมือแก้ไขคุณสมบัติของ Field ผ่าน Design View เช่น การเปลี่ยนจากข้อความ (VARCHAR) ที่เก็บตัวเลข ให้กลายเป็นจำนวนเต็ม (INT) เพื่อลดขนาดการจัดเก็บและทำให้การประมวลผลคำสั่ง Query รวดเร็วขึ้น



2.การเชื่อมต่อและดึงข้อมูล (Database Connectivity):
  จัดการทำ Seamless Connection ระหว่างฐานข้อมูล SQL และเครื่องมือวิเคราะห์ เพื่อให้มั่นใจว่าข้อมูลไหลเข้าสู่ Pipeline ได้อย่างถูกต้อง 100%



3.กระบวนการ ETL และการทำ Data Casting:
  ใช้ Power Query เป็นเครื่องมือหลักในการทำความสะอาดข้อมูล
  ดำเนินการ Data Casting หรือการแปลงประเภทข้อมูลในขั้นตอนสุดท้าย เช่น การจัดการรูปแบบวัน/เวลา (Date/Time) และความละเอียดของจุดทศนิยม (Decimal Precision) เพื่อป้องกันการเกิด "Data Loss" หรือข้อมูลเพี้ยนระหว่างย้ายจากฐานข้อมูลมายังรายงาน




# สิ่งที่ได้รับจากการทำ Lab นี้ (Key Outcomes & Takeaways)
กระบวนการนี้ไม่ใช่แค่การกดคลิกตามขั้นตอน แต่คือแก่นของการทำ ETL (Extract, Transform, Load) เพื่อให้ได้ Data Quality ที่ดีครับ สิ่งที่คุณได้กลับมาคือ:

ทักษะการตรวจสอบต้นทาง (Extraction & Profiling): รู้วิธีเข้าถึงข้อมูลดิบจาก SQL Database และตรวจสอบชนิดของข้อมูลตั้งแต่ระดับ Schema เพื่อป้องกันข้อผิดพลาดในการดึงข้อมูล

ความเข้าใจเรื่องบริบทของข้อมูล (Data Context): ได้เรียนรู้ว่าไม่ใช่ตัวเลขทุกตัวควรมี Data Type เป็นตัวเลขเสมอไป เช่น EnrollmentID แม้หน้าตาจะเป็นตัวเลข แต่มันคือ "รหัสประจำตัว" ที่เราจะไม่นำมาบวก ลบ คูณ หาร กัน การแปลงประเภทข้อมูลเป็น Text จะช่วยป้องกันไม่ให้โปรแกรมวิเคราะห์ข้อมูลนำไปคำนวณทางคณิตศาสตร์แบบผิดวัตถุประสงค์

ทักษะการทำ Data Cleaning เบื้องต้น (Transformation): สามารถใช้งานเครื่องมือเตรียมข้อมูลอย่าง Power Query Editor ได้ ซึ่งทักษะการจัดเตรียมข้อมูลดิบให้พร้อม ถูกต้อง และคลีนที่สุดก่อนนำไปวิเคราะห์ต่อ เป็นทักษะที่ใช้จริงในการทำงานสาย Data Analytics เป็นประจำทุกวัน



