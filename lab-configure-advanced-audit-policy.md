# 🔐 Lab: Configure Advanced Audit Policy
> _การตั้งค่า Advanced Audit Policy_

![Step 0](images/lab-configure-advanced-audit-policy/0.png)
---

### 📋 โจทย์

คุณทำงานเป็นผู้ดูแลระบบความปลอดภัย IT ของบริษัทขนาดเล็ก ในโครงการปรับปรุงความปลอดภัยอย่างต่อเนื่อง คุณต้องการตั้งค่านโยบายการตรวจสอบ (audit policy) สำหรับเครื่องคอมพิวเตอร์ทั้งหมด เพื่อตรวจสอบการพยายามเข้าสู่ระบบและเหตุการณ์สำคัญอื่นๆ

**งานของคุณคือ:** ตั้งค่านโยบายการตรวจสอบต่างๆ ใน WorkstationGPO ตามที่กำหนด

---

### 🔹 ส่วนที่ 1: Local Policies

| Local Policies | Setting |
|--------|------------|
| Audit: Force audit policy subcategory settings (Windows Vista or later) to override audit policy category settings | **Enabled** |
| Audit: Shut down system immediately if unable to log security audits | **Enabled** |

---

### 🔹 ส่วนที่ 2: Event Log (บันทึกเหตุการณ์)

| Event Log | Setting |
|-----------|---------|
| Retention method for security log | **Do not overwrite events (clear log manually)** |

---

### 🔹 ส่วนที่ 3: Advanced Audit Policy Configuration

| Advanced Audit Policy Configuration | Setting |
|--------------------------------------|---------|
| Account Logon: Audit Credential Validation | **Success and Failure** |
| Account Management: Audit User Account Management | **Success and Failure** |
| Account Management: Audit Security Group Management | **Success and Failure** |
| Account Management: Audit Other Account Management Events | **Success and Failure** |
| Account Management: Audit Computer Account Management | **Success** |
| Detailed Tracking: Audit Process Creation | **Success** |
| Logon/Logoff: Audit Logon | **Success and Failure** |
| Logon/Logoff: Audit Logoff | **Success** |
| Policy Change: Audit Authentication Policy Change | **Success** |
| Policy Change: Audit Audit Policy Change | **Success and Failure** |
| Privilege Use: Audit Sensitive Privilege Use | **Success and Failure** |
| System: Audit System Integrity | **Success and Failure** |
| System: Audit Security System Extension | **Success and Failure** |
| System: Audit Security State Change | **Success and Failure** |
| System: Audit IPsec Driver | **Success and Failure** |

---

**⚠️ ห้ามใช้เมนู Audit แบบเก่าใน**
```
Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Audit Policies
```

---

## ขั้นตอนการทำ

### ขั้นตอนที่ 1 เปิดเครื่องมือ Group Policy (GPMC)
ที่มุมขวาบนของ Server Manager จะมีปุ่ม Tools
![Step 1](images/lab-configure-advanced-audit-policy/1.png)

ในเมนูที่เด้งลงมา ให้เลือก Group Policy Management
![Step 2](images/lab-configure-advanced-audit-policy/2.png)

ก็จะมีหน้าต่างใหม่เปิดขึ้นมา นี่คือเครื่องมือหลักที่จะต้องใช้
![Step 3](images/lab-configure-advanced-audit-policy/3.png)

### ขั้นตอนที่ 2 - หา WorkstationGPO
ในหน้าต่าง Group Policy Management ที่เปิดขึ้นมา ให้ไปที่
Forest → Domains → CorpNet.local → Group Policy Objects ในนั้นจะมี WorkstationGPO
![Step 4](images/lab-configure-advanced-audit-policy/4.png)

เมื่อเจอแล้ว ให้คลิกขวาที่ WorkstationGPO และเลือก Edit
![Step 5](images/lab-configure-advanced-audit-policy/5.png)

จะมีหน้าต่างชื่อ Group Policy Management Editor นี่คือทั้งหมดที่ต้องตั้งค่าตามโจทย์
![Step 6](images/lab-configure-advanced-audit-policy/6.png)

### ส่วนที่ 1: Local Policies
จากหน้าต่างที่พึ่งเปิด ให้ไปที่ Computer Configurati → Policies → Windows Settings → Security Settings → Local Policies → Security Options
![Step 7](images/lab-configure-advanced-audit-policy/7.png)

ดับเบิลคลิกที่ Audit: Force audit policy subcategory settings (Windows Vista or later) to override audit policy category settings
![Step 8](images/lab-configure-advanced-audit-policy/8.png)

ติ๊ก Checkbox Define this policy setting ก่อน แล้วจะเลือก radio box ข้างล่างได้ ให้เลือก **Enabled** และกด OK
![Step 9](images/lab-configure-advanced-audit-policy/9.png)

และ Audit: Shut down system immediately if unable to log security audits เป็น **Enabled** เช่นกัน
![Step 10](images/lab-configure-advanced-audit-policy/11.png)

จะมีหน้าต่าง confirm มาถามว่า แน่ใจไหมที่จะเปลี่ยนค่านี้ เพราะค่าที่เรากำลังเปิด เป็นค่าที่มีผลกระทบกับระบบได้จริง ให้เรากดตกลง
![Step 12](images/lab-configure-advanced-audit-policy/12.png)

### ส่วนที่ 2: ตั้งค่า Event Log
ไปที่ Computer Configuration → Policies → Windows Settings → Security Settings → Event Log
![Step 13](images/lab-configure-advanced-audit-policy/13.png)

ดับเบิลคลิกที่ Retention method for security log
![Step 14](images/lab-configure-advanced-audit-policy/14.png)

แล้วติ๊ก Define → เลือก Do not overwrite events (clear log manually) และกด OK
![Step 15](images/lab-configure-advanced-audit-policy/15.png)

### ส่วนที่ 3: Advanced Audit Policy Configuration
ไปที่ Computer Configuration → Policies → Windows Settings → Security Settings → Advanced Audit Policy Configuration → Audit Policies และหลังจากนี้ ทำตามตารางสุดท้าย
![Step 16](images/lab-configure-advanced-audit-policy/16.png)

Account Logon: Audit Credential Validation : **Success and Failure** ✔️
![Step 17](images/lab-configure-advanced-audit-policy/17.png)

Account Management: Audit User Account Management : **Success and Failure** ✔️
![Step 18](images/lab-configure-advanced-audit-policy/18.png)

Account Management: Audit Security Group Management : **Success and Failure** ✔️
![Step 19](images/lab-configure-advanced-audit-policy/19.png)

Account Management: Audit Other Account Management Events : **Success and Failure** ✔️
![Step 20](images/lab-configure-advanced-audit-policy/20.png)

Account Management: Audit Computer Account Management : **Success** ✔️
![Step 21](images/lab-configure-advanced-audit-policy/21.png)

Detailed Tracking: Audit Process Creation : **Success** ✔️
![Step 22](images/lab-configure-advanced-audit-policy/22.png)

Logon/Logoff: Audit Logon : **Success** and Failure ✔️
![Step 23](images/lab-configure-advanced-audit-policy/23.png)

Logon/Logoff: Audit Logoff : **Success** ✔️
![Step 24](images/lab-configure-advanced-audit-policy/24.png)

Policy Change: Audit Authentication Policy Change : **Success** ✔️
![Step 25](images/lab-configure-advanced-audit-policy/25.png)

Policy Change: Audit Audit Policy Change : **Success and Failure** ✔️
![Step 26](images/lab-configure-advanced-audit-policy/26.png)

Privilege Use: Audit Sensitive Privilege Use : **Success and Failure** ✔️
![Step 27](images/lab-configure-advanced-audit-policy/27.png)

System: Audit System Integrity : **Success and Failure** ✔️
![Step 28](images/lab-configure-advanced-audit-policy/28.png)

System: Audit Security System Extension : **Success and Failure** ✔️
![Step 29](images/lab-configure-advanced-audit-policy/29.png)

System: Audit Security State Change : **Success and Failure** ✔️
![Step 30](images/lab-configure-advanced-audit-policy/30.png)

System: Audit IPsec Driver : **Success and Failure** ✔️
![Step 31](images/lab-configure-advanced-audit-policy/31.png)

### Done 🎉
![Step 32](images/lab-configure-advanced-audit-policy/32.png)

---

## สรุป
Lab นี้เป็นการฝึกตั้งค่า Advanced Audit Policy บน Windows Server ผ่าน Group Policy Management เพื่อเพิ่มความปลอดภัยในการตรวจสอบเหตุการณ์สำคัญ โดยครอบคลุม 3 ส่วนหลัก:

1. **Local Policies** - เปิดใช้งานการบังคับใช้ Audit Policy Subcategory และตั้งค่าให้ระบบปิดทันทีหากไม่สามารถบันทึก Security Audit ได้
2. **Event Log** - กำหนดให้ Security Log ไม่ถูกเขียนทับโดยอัตโนมัติ ต้องลบด้วยตนเอง
3. **Advanced Audit Policy Configuration** - ตั้งค่าการตรวจสอบรายละเอียด 15 หมวดหมู่ ครอบคลุมทั้ง Account Logon, Account Management, Process Creation, Logon/Logoff, Policy Change, Privilege Use และ System เพื่อติดตามเหตุการณ์ทั้งที่สำเร็จและล้มเหลว

การตั้งค่าเหล่านี้ช่วยให้สามารถตรวจจับและตอบสนองต่อภัยคุกคามความปลอดภัยได้ทันท่วงที รวมถึงเก็บหลักฐานสำหรับการตรวจสอบย้อนหลัง

---

[← กลับหน้าแรก](README.md)
