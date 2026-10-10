# [ANANTA] TH Beta Private Server

[![Discord Shield](https://img.shields.io/badge/Discord-Join%20Community-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/t7vMBJRDwU)

ระบบจัดการเซิร์ฟเวอร์จำลองและ Launcher สำหรับโปรเจกต์ Ananta

![Ananta Preview](./image.png)

---

## 📌 คุณสมบัติหลัก (Features)

- **AnantaDEV.exe:** GUI Launcher หลักสำหรับควบคุมการเปิด-ปิด Server และ Injector
- **Web Console / API:** ระบบจัดการและเช็กสถานะผ่านเว็บเบราว์เซอร์ที่ [http://127.0.0.1:17888/](http://127.0.0.1:17888/)
- **Drmk.Server:** ระบบเซิร์ฟเวอร์หลักสำหรับการจัดการข้อมูล
- **Drmk.Proxy:** พร็อกซีเซิร์ฟเวอร์จัดการการเชื่อมต่อเครือข่าย
- **Drmk.SDK:** ไลบรารีเครื่องมือและโครงสร้างข้อมูลสำหรับนักพัฒนา

---

## 📦 สิ่งที่ต้องติดตั้งก่อนใช้งาน (Prerequisites)

สำหรับ Windows กรุณาดาวน์โหลดและติดตั้งโปรแกรมจำเป็นต่อไปนี้ก่อนเริ่มใช้งาน:

- **Visual Studio Code:** [ดาวน์โหลด Visual Studio Code](https://code.visualstudio.com/)
- **7-Zip:** [ดาวน์โหลด 7-Zip](https://www.7-zip.org/)
- **Rust:** [ดาวน์โหลด Rust (rustup-init.exe 64-bit)](https://www.rust-lang.org/tools/install)
- **Python:** [ดาวน์โหลด Python (Windows 64-bit)](https://www.python.org/downloads/windows/)
- **.NET 8.0 Runtime / SDK:** [ดาวน์โหลด .NET 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- **Node.js:** [ดาวน์โหลด Node.js](https://nodejs.org/en)
- **Visual Studio (C++ Workloads):** [ดาวน์โหลด Visual Studio](https://visualstudio.microsoft.com/downloads/)

### 🛠️ คำแนะนำการติดตั้งโปรแกรมจำเป็น

<details>
<summary><b>1. Visual Studio Code</b></summary>

1. ดาวน์โหลดตัวติดตั้ง **VS Code (Windows x64)** จากเว็บไซต์หลัก
2. ดับเบิลคลิกเปิดไฟล์ติดตั้ง `.exe`
3. เลือก **I accept the agreement** (ยอมรับข้อตกลงใช้งาน) แล้วกด **Next**
4. ในหน้าเลือกตัวเลือกเพิ่มเติม แนะนำให้ติ๊กเลือก:
   - **Create a desktop icon** (สร้างไอคอนบนหน้าจอ)
   - **Add "Open with Code" to Windows Explorer file context menu** (เพิ่มเมนูเปิดด้วย VS Code เมื่อคลิกขวาที่ไฟล์)
   - **Add "Open with Code" to Windows Explorer directory context menu** (เพิ่มเมนูเปิดด้วย VS Code เมื่อคลิกขวาที่โฟลเดอร์)
5. กด **Next** แล้วกด **Install**
6. เมื่อติดตั้งเสร็จแล้ว สามารถเปิดโปรแกรมขึ้นมา เลือกระธีมหน้าตา (Dark / Light) แล้วเริ่มใช้งานได้ทันที
</details>

<details>
<summary><b>2. 7-Zip & Rust</b></summary>

**การติดตั้ง 7-Zip:**
1. ดาวน์โหลดไฟล์ติดตั้งแบบ 64-bit (`.exe`) จากเว็บไซต์ 7-Zip
2. ดับเบิลคลิกเปิดไฟล์และติดตั้งตามขั้นตอนปกติ

**การติดตั้ง Rust:**
1. ดับเบิลคลิกที่ไฟล์ติดตั้ง (`rustup-init.exe`)
2. เริ่มการติดตั้ง Rust หากโปรแกรมไม่เด้งหลุดออก
3. ในตัวเลือกการติดตั้ง ให้กด **Enter** เพื่อใช้ค่าเริ่มต้น
4. พิมพ์ `1` แล้วกด **Enter** (*Proceed with installation*)
5. เมื่อการติดตั้งเสร็จสมบูรณ์ ให้กด **Enter** แล้วปิดหน้าต่างโปรแกรมออกไป
</details>

<details>
<summary><b>3. Node.js</b></summary>

1. เปิดไฟล์ติดตั้ง Node.js
2. ติดตั้งโปรแกรมและรอจนกระทั่งขึ้นหน้าต่าง **Node.js®**
3. เปิดโปรแกรม **Node.js**
4. เสร็จสิ้นกระบวนการเตรียมการใช้งาน Node.js
</details>

<details>
<summary><b>4. Visual Studio (C++ Workloads)</b></summary>

1. เปิดโปรแกรม Visual Studio Installer และรอจนกว่ากระบวนการเตรียมการจะเสร็จสิ้น
2. คุณต้องมี Visual Studio C++ เพื่อเรียกใช้ไฟล์ดาวน์โหลด Rust (หากยังไม่มีโปรแกรมติดตั้ง ให้ดาวน์โหลดจากลิงก์ด้านบน)
3. เลือกติ๊กหัวข้อ Build Tools / Workloads ดังต่อไปนี้:
   - **.NET desktop development**
   - **Desktop development with C++**
   - **Game development with C++**
4. กดเริ่มการดาวน์โหลดและติดตั้งไฟล์ C++
5. โปรดรอจนกว่าการแตกไฟล์และการดาวน์โหลดทั้งหมดจะเสร็จสิ้น
6. เมื่อการติดตั้งเสร็จสมบูรณ์ ให้ปิดโปรแกรม Visual Studio ออกไป
</details>

---


## 🚀 วิธีการเริ่มต้นใช้งาน (Getting Started)

1. ติดตั้งโปรแกรมจำเป็น (VS Code, 7-Zip, Rust, Python, .NET 8.0, Node.js และ Visual Studio C++) ให้เรียบร้อย
2. ดาวน์โหลดตัวเกม Patch และไฟล์ Server นำมาวางไว้ในโฟลเดอร์โปรเจกต์
3. ดับเบิลคลิกเปิดโปรแกรม **`AnantaDEV.exe`**
4. ในหน้าต่าง **Ananta Launcher**:
* เลือก **Game Path** ไปยังตำแหน่งโฟลเดอร์เกมของคุณ
* กดปุ่ม **Start server** เพื่อเริ่มต้นการทำงาน
* ตรวจสอบสถานะเซิร์ฟเวอร์ผ่านเบราว์เซอร์ที่ `http://127.0.0.1:17888/`
* กด **Launch game** เพื่อเข้าสู่เกม

---

## ⚙️ การตั้งค่าเพิ่มเติมใน Launcher

* **Install certificate:** ติดตั้งใบรับรองความปลอดภัย (แก้ปัญหา "failed to get config info")
* **Install fast-start patch:** ข้ามดีเลย์ช่วงเริ่มต้นเซิร์ฟเวอร์
* **Traffic / Crowd / Destructible:** สวิตช์เปิด-ปิดการจราจร ฝูงชน และวัตถุในฉาก
* **Show console window:** เปิดหน้าต่างคอนโซลสำหรับตรวจสอบ/แก้ปัญหา

---


> *หมายเหตุ: โปรเจกต์นี้จัดทำขึ้นเพื่อการศึกษาและการพัฒนาทดสอบเท่านั้น*
