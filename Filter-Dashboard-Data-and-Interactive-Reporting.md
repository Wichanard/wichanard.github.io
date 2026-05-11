# 📊 Live Lab: Filter Dashboard Data & Interactive Reporting
CompTIA Data+ (DA0-001) Implementation
📝 Project Overview (ภาพรวมโครงการ)
In this project, I acted as a Data Analyst designing a client-facing dashboard. The primary goal was to balance data security and user experience by implementing a multi-layered filtering system. I built a dynamic reporting solution that allows users to drill down into specific student extracurricular activities while maintaining control over data visibility.



# โปรเจกต์นี้เป็นการสวมบทบาท Data Analyst ในการออกแบบ Dashboard เพื่อนำเสนอข้อมูลให้ลูกค้า โดยเน้นการจัดการระบบตัวกรอง (Filtering) หลายระดับ เพื่อควบคุมการเข้าถึงข้อมูลที่จำเป็นและสร้างประสบการณ์การใช้งานที่ดี (User Experience) ผ่านการสร้างรายงานที่โต้ตอบได้ (Interactive Report) เกี่ยวกับกิจกรรมนอกหลักสูตรของนักเรียน



# ภาพที่ 1: การสำรวจแหล่งข้อมูล (Data Source Exploration)
<img width="582" height="355" alt="2 1" src="https://github.com/user-attachments/assets/4fde03e2-53b0-4857-97a7-5bde187a2be4" />

สิ่งที่กำลังทำ: คือเรากำลังใช้งาน Microsoft SQL Server Management Studio (SSMS) เพื่อสำรวจฐานข้อมูล TDHS_StudentInfoSys
รายละเอียด: มีการคลิกขวาที่ตาราง dbo.tblEnrollment และเตรียมใช้คำสั่ง Select Top 1000 Rows นี่คือขั้นตอนแรกในการทำ Data Profiling เพื่อขอดูหน้าตาข้อมูลคร่าวๆ ว่ามีลักษณะอย่างไรก่อนนำไปดึงไปประมวลผลต่อ



# ภาพที่ 2: การตรวจสอบโครงสร้างข้อมูล (Schema & Data Type Inspection)
<img width="552" height="512" alt="2 2" src="https://github.com/user-attachments/assets/a80e6395-9e16-4a53-911e-7976cff30de3" />

สิ่งที่กำลังทำ: เปิดดูหน้า Design ของตาราง dbo.tblEnrollment เพื่อตรวจสอบ Data Dictionary หรือ Schema ของตารางนี้
รายละเอียด: ระบบแสดงให้เห็นชื่อคอลัมน์และ Data Type ต้นทางอย่างชัดเจน เช่น EnrollmentID เก็บเป็น int (ตัวเลขจำนวนเต็ม), EnrollmentDate เป็น datetime (วันและเวลา) และ SchYr_Grade เป็น nvarchar(2) (ข้อความ) การรู้ว่าระบบฐานข้อมูลต้นทางเก็บข้อมูลมาแบบไหน จะช่วยให้เราวางแผนแปลงข้อมูลได้อย่างถูกต้อง



# ภาพที่ 3: การแปลงประเภทข้อมูล (Data Type Conversion)
<img width="416" height="561" alt="2 3" src="https://github.com/user-attachments/assets/ed758ff8-9bc5-4ef7-931e-f96a324c0e4f" />

สิ่งที่กำลังทำ: ข้อมูลถูกดึงเข้ามาใน Power Query Editor เพื่อทำการแปลงข้อมูล (Data Transformation)
รายละเอียด: คุณกำลังคลิกเมนู Dropdown ที่หัวคอลัมน์ EnrollmentID เพื่อเปลี่ยนประเภทข้อมูล (Change Type) โดยกำลังจะเปลี่ยนจากตัวเลขให้กลายเป็น Text (ข้อความ)



# สิ่งที่ได้รับจากการทำ Lab นี้ (Key Outcomes & Takeaways)
คือแก่นของการทำ ETL (Extract, Transform, Load) เพื่อให้ได้ Data Quality 

ทักษะการตรวจสอบต้นทาง (Extraction & Profiling): รู้วิธีเข้าถึงข้อมูลดิบจาก SQL Database และตรวจสอบชนิดของข้อมูลตั้งแต่ระดับ Schema เพื่อป้องกันข้อผิดพลาดในการดึงข้อมูล

ความเข้าใจเรื่องบริบทของข้อมูล (Data Context): ได้เรียนรู้ว่าไม่ใช่ตัวเลขทุกตัวควรมี Data Type เป็นตัวเลขเสมอไป เช่น EnrollmentID แม้หน้าตาจะเป็นตัวเลข แต่มันคือ "รหัสประจำตัว" ที่เราจะไม่นำมาบวก ลบ คูณ หาร กัน การแปลงประเภทข้อมูลเป็น Text จะช่วยป้องกันไม่ให้โปรแกรมวิเคราะห์ข้อมูลนำไปคำนวณทางคณิตศาสตร์แบบผิดวัตถุประสงค์

ทักษะการทำ Data Cleaning เบื้องต้น (Transformation): สามารถใช้งานเครื่องมือเตรียมข้อมูลอย่าง Power Query Editor ได้ ซึ่งทักษะการจัดเตรียมข้อมูลดิบให้พร้อม ถูกต้อง และคลีนที่สุดก่อนนำไปวิเคราะห์ต่อ เป็นทักษะที่ใช้จริงในการทำงานสาย Data Analytics เป็นประจำทุกวัน



