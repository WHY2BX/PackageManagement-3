# PackageManagement-3
COMPUTER ORGANIZATION AND OPERATING SYSTEM (Chapter: Package Management, Section: 3)

## Introduction to Package Management ##
  Ubuntu มีระบบในการจัดการ Package ที่ครอบคลุมสำหรับ การติดตั้ง, อัพเกรด, กำหนดค่า รวมไปถึงการ ลบ Software นอกจากนี้ยังสามารถตรวจสอบและเข้าถึงฐานข้อมูลที่มีองค์ประกอบมากกว่า 60,000 Software packages อีกด้วย 
  

- ### Package คืออะไร ? ###
  แพ็คเกจ (package) ใน Linux ก็เปรียบเสมือน Program บน Window ซึ่งจะประกอบไปด้วย หลายๆไฟล์ที่ใช้ในการทำงาน เช่น การติดตั้งโปรแกรมในลีนุกซ์ตระกูล Debian

- ### Package Management Tools ###

  เป็นเครื่องมือที่ใช้ในการจัดการ Package ทั้งติดตั้ง และถอนการติดตั้ง มีตั้งแต่ simple command-line ไปจนถึง Interface Graphics ที่ใช้ง่ายเหมาะสำหรับมือใหม่ที่กำลังหัดใช้ Ubuntu และทำให้การติดตั้งและจัดการซอฟต์แวร์บนระบบ Linux ง่ายขึ้น
  Linux มี Package Management Tools มากมายหลายชนิด แต่ที่นิยมใช้กัน ได้แก่
  - apt และ apt-get ใช้บนระบบ Debian และ Ubuntu
  - yum ใช้บนระบบ Red Hat และ CentOS
  - dnf (Dandified yum) ใช้แทน yum บนระบบ Fedora
  - zypper ใช้บนระบบ openSUSE

  ซึ่ง Tools เหล่านี้ก็มีคุณสมบัติที่คล้ายคลึงกัน รวมถึงมีข้อดีและข้อเสียที่แตกต่างกันไป โดยเกณฑ์จะขึ้นอยู่กับความชอบของผู้ใช้ และระบบ Linux ที่ใช้ ทำให้ไม่มีข้อสรุปว่า Tools ไหนดีที่สุด

## Introduction to Repository Setup ##
- ### Respository คืออะไร? ###
    Respository เป็นคลัง Package เวลาเราจะติดตั้งโปรแกรมอะไร ก็ไปดาวน์โหลด Package ของโปรแกรมนั้นๆ ตาม Respository ที่มันอยู่ ซึ่งโดยปกติแล้ว พวก Respository จะอยู่บน Internet เพื่อให้เครื่องที่สามารถเชื่อมต่อ Internet ได้ สามารถ Update Software ได้อย่างสม่ำเสมอ แต่บางครั้งการ Update ผ่าน Internet อาจจะเปลือง Traffic การทำ Local Respository ก็อาจจะตอบโจทย์มากกว่า ซึ่ง Package เหล่านี้ก็มีการแบ่ง ตาม Distribution ที่ใช้ด้วย เช่น ตระกูล Redhat/Fedora/SUSE จะใช้ไฟล์ .rpm แต่ถ้าเป็นตระกูล Debian/Ubuntu ก็จะใช้ไฟล์ .deb ซึ่งไม่สามารถใช้ร่วมกันได้ สามารถแบ่งได้หลักๆ 2 ประเภท
  - Official Repository
    จัดทำโดยผู้พัฒนาหรือผู้จัดจำหน่าย Linux ผ่านการทดสอบ และมีความเสถียรสูง
  - Unofficial Repository
    จัดทำโดยนักพัฒนาจากภายนอก มักมี Software Version ล่าสุด หรือ ซอฟต์แวร์ที่ไม่มีใน Repository ทาง Official
- ### ทำ Respository Setup ไปเพื่ออะไร? ###
  - **การจัดการ Software**
    - ทำให้สามารถ ติดตั้ง / อัปเดต / ลบ ได้สะดวกมากขึ้น โดยไม่ต้องดาวน์โหลดและคอมไพล์จากต้นทาง
    - ทำให้สามารถควบคุม Version ของ Software บนเครื่องได้
    - มั่นใจได้ว่าระบบสามารถทำงานได้อย่างสม่ำเสมอ และมีความปลอดภัย
    - ทำให้สามารถ Update Software เป็น Version ล่าสุด หรือ เลือกติดตั้ง Software ใน Version ที่ต้องการได้
  - **การแบ่งปัน Software**
    -  ทำให้ผู้พัฒนา สามารถแบ่งปัน Software ของตนเอง ให้แก่ผู้อื่นได้อย่างง่ายดาย
    -  ทำให้ผู้ใช้ สามารถค้นหาและติดตั้ง Open Source Software ได้สะดวกมากขึ้น
    -  ทำให้ผู้ใช้ สามารถสร้างและใช้งาน Software ภายในองค์กร ได้อย่างมีประสิทธิภาพ
  - **การสำรองข้อมูล**
    -  สำรอง Data และ Settings ต่างๆได้สะดวกมากขึ้น
    -  กู้คืน Data และ Settings ได้ง่าย
    -  จัดการ ควบคุม การสำรองและกู้คืน Data ได้อย่างมีประสิทธิภาพ
  

## Referenecs ##
### Mainpage ###
-  https://feversecure.wordpress.com/2017/10/18/วิธีใช้-apt-get-บน-linux-ฉบับง่ายๆ/#:~:text=*แพ็คเกจ%20(package)%20ใน%20Linux,สำหรับหา%20packages%20ใหม่ๆ
- https://suchart.wordpress.com/debianubuntu-package-management/
- https://bard.google.com/chat/3cc46de7841e2fc6
- https://jetsadamalaisirirat.medium.com/การทำ-local-repository-สำหรับ-redhat-centos-ece9c4545960
- https://bigta.wordpress.com/2011/04/30/installing-program-in-linux/ 

## Members ##
-
-
-
- 65070233 สหัสวรรษ วงศ์บุญธเนธ
- 65070238 น.ส.สิริมงคล ทองขวัญใจ
- 65070241 น.ส.สุพิชชา วิเศษเจริญ
