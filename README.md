# Ananta - Server & Client Launcher

ระบบจัดการเซิร์ฟเวอร์จำลองและ Launcher สำหรับโปรเจกต์ Ananta

![Ananta Preview](./image.png)

## 📌 คุณสมบัติหลัก (Features)

- **AnantaDEV.exe:** GUI Launcher หลักสำหรับควบคุมการเปิด-ปิด Server และ Injector
- **Web Console / API:** ระบบจัดการและเช็กสถานะผ่านเว็บเบราว์เซอร์ที่ [http://127.0.0.1:17888/](http://127.0.0.1:17888/)
- **Drmk.Server:** ระบบเซิร์ฟเวอร์หลักสำหรับการจัดการข้อมูล
- **Drmk.Proxy:** พร็อกซีเซิร์ฟเวอร์จัดการการเชื่อมต่อเครือข่าย
- **Drmk.SDK:** ไลบรารีเครื่องมือและโครงสร้างข้อมูลสำหรับนักพัฒนา

## 🛠️ ข้อกำหนดและเครื่องมือ (Prerequisites)

เอกสารนี้อธิบายการใช้งานบน Windows เครื่องมือสำหรับพัฒนาและสร้างส่วนประกอบอาจแตกต่างกันตามส่วนของโปรเจกต์ที่ต้องการใช้งาน:

- **.NET 8.0 SDK:** สำหรับสร้างหรือพัฒนาส่วนประกอบที่ใช้ .NET
- **Rust (64-bit):** สำหรับส่วนประกอบที่พัฒนาด้วย Rust
- **Python:** สำหรับสคริปต์และเครื่องมือที่เกี่ยวข้อง
- **Node.js:** สำหรับเครื่องมือหรือส่วนติดต่อเว็บที่ใช้ Node.js
- **Visual Studio Build Tools:** เลือก workload **Desktop development with C++** เมื่อต้องสร้างส่วนประกอบภาษา C++ หรือ Rust ที่ต้องใช้ตัวเชื่อมโยง C++
- **Visual Studio Code:** โปรแกรมแก้ไขโค้ดที่แนะนำ

*การใช้งาน Launcher ที่สร้างไว้แล้วอาจไม่จำเป็นต้องติดตั้งเครื่องมือสำหรับพัฒนาทั้งหมด ให้ตรวจสอบข้อกำหนดของส่วนประกอบที่ต้องการใช้งานก่อนติดตั้ง*

### 🔗 ดาวน์โหลดเครื่องมือจากเว็บไซต์ทางการ:

- [Visual Studio Code](https://code.visualstudio.com/)
- [Rust](https://www.rust-lang.org/tools/install)
- [Python สำหรับ Windows](https://www.python.org/downloads/windows/)
- [.NET 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- [Node.js](https://nodejs.org/)
- [Visual Studio](https://visualstudio.microsoft.com/downloads/)

## 📥 ดาวน์โหลดไฟล์ระบบและตัวเกม (Downloads)

- **GAME ANANTA (81.4 GB):** [ดาวน์โหลดตัวเกมผ่าน Gofile](https://gofile.io/d/AoWrjNoG)
- **Patch Files (.dll):** [ดาวน์โหลดไฟล์ Patch (.dll) ผ่าน Transfer.it](https://transfer.it/t/rnH5BM1hGR4Y)
- **Fix Device ID Error (Netease.zip):** [ดาวน์โหลด Netease.zip](https://cdn.discordapp.com/attachments/1550411381050712064/1550418157196550244/Netease.zip?ex=6ac6a6ae&is=6ac5552e&hm=fdb04995b96f41f149ee26a07692e929d1bf369b1df38c22bc8f2770ce8812e3&)
- **Full Server Assets (.tar.zst):** [ดาวน์โหลดไฟล์ Server ผ่าน Transfer.it](https://transfer.it/t/cinoqA4X0bib)

### 📂 วิธีติดตั้งตัวเกมและ Patch
1. **การติดตั้ง Patch:** นำไฟล์ `.dll` ที่ดาวน์โหลดมา ไปวางไว้ในโฟลเดอร์ตัวเกม ANANTA
2. **การแก้ไข device_id error:** แตกไฟล์ `Netease.zip` แล้วนำโฟลเดอร์ไปวางไว้ที่ตำแหน่ง:
   `C:\Users\<your_account_name>\AppData\Roaming\`
3. **การแตกไฟล์ Server (.tar.zst):**
   - **ใช้ 7-Zip:** คลิกขวาที่ไฟล์ `AnantaPS-TH.tar.zst` > เลือก `7-Zip` > `Extract Here` (จะได้ไฟล์ `.tar`) จากนั้นคลิกขวาที่ไฟล์ `.tar` แล้วเลือก `Extract Here` อีกครั้ง
   - **ใช้ PowerShell:** เปิด PowerShell ในโฟลเดอร์แล้วพิมพ์คำสั่ง `tar -axvf AnantaPS-TH.tar.zst`

## 🚀 วิธีใช้งานทั่วไป

1. ติดตั้งโปรแกรมจำเป็นที่เกี่ยวข้องให้เรียบร้อย
2. ดาวน์โหลดตัวเกม Patch และไฟล์ Server นำมาวางไว้ในโฟลเดอร์โปรเจกต์
3. ดับเบิลคลิกเปิดโปรแกรม **`AnantaDEV.exe`**
4. ในหน้าต่าง **Ananta Launcher**:
   - เลือก **Game Path** ไปยังตำแหน่งโฟลเดอร์เกมของคุณ
   - กดปุ่ม **Start server** เพื่อเริ่มต้นการทำงาน
   - ตรวจสอบสถานะเซิร์ฟเวอร์ผ่านเบราว์เซอร์ที่ `http://127.0.0.1:17888/`
   - กด **Launch game** เพื่อเข้าสู่เกม
5. เมื่อใช้งานเสร็จ ให้หยุดเซิร์ฟเวอร์จาก Launcher ก่อนปิดโปรแกรม

## ⚙️ การตั้งค่าใน Launcher

- **Install certificate:** ติดตั้งและจัดการใบรับรองความปลอดภัยที่ Launcher ใช้ (แก้ปัญหา "failed to get config info")
- **Install fast-start patch:** เปิดใช้ตัวเลือกเริ่มต้นเซิร์ฟเวอร์แบบรวดเร็ว ข้ามดีเลย์ช่วงเริ่มต้นเซิร์ฟเวอร์
- **Traffic / Crowd / Destructible:** สวิตช์เปิดหรือปิดองค์ประกอบการจราจร ฝูงชน และวัตถุในฉาก
- **Show console window:** แสดงหน้าต่างคอนโซลเพื่อดูข้อความสถานะและช่วยตรวจสอบปัญหา

หากพบปัญหา ให้ตรวจสอบสถานะใน Launcher และข้อความในคอนโซลก่อน จากนั้นตรวจสอบว่าเซิร์ฟเวอร์เริ่มทำงานแล้วและเปิด Web Console จากเครื่องเดียวกัน

---

*หมายเหตุ: โปรเจกต์นี้จัดทำขึ้นเพื่อการศึกษาและการพัฒนาทดสอบเท่านั้น*