# ใบงานการทดลองที่ 1: การออกแบบรายวิชาและสร้าง Activities 

---

## 📋 ข้อมูลกิจกรรม

**ชื่อกิจกรรม:** การสร้างรายวิชาใน Moodle ตาม Best Practice Flow และฝึกสร้าง Activities ทุกประเภท

**วัตถุประสงค์เชิงพฤติกรรม:** นักศึกษาสามารถ:

1. ✅ ตั้งค่ารายวิชาพื้นฐานตาม Best Practice Flow
2. ✅ สร้าง Gradebook Categories และ Groups อย่างถูกต้อง
3. ✅ สร้าง Activities  **Attendance, Page, Lesson, Assignment, Choice, Quiz, H5P** ได้
4. ✅ กำหนดตัวเลือก Grade, Restrict Access, Completion, Group Submission ได้ถู  กต้องตามความต้องการ
5. ✅ สร้าง Question Bank และสุ่มคำถามใน Quiz ได้


**คำแนะนำ:**
- 📌 เลือกรายวิชาและหัวข้อตามที่กำหนดไว้ใน NotebookLM
- 📌 สร้าง Activities ตามโจทย์และข้อกำหนดที่กำหนด

---

## 📝 ขั้นตอนการปฏิบัติ 

```
⚙️  1. Course Settings
          ↓
📊 2. Setup Gradebook
          ↓
👥 3. Create Groups
          ↓
📂 4. Organize Sections
          ↓
💾 5. Build Question Bank
          ↓
📝 6. สร้าง Activities  7 ประเภท
   ├─ 6.1 Attendance
   ├─ 6.2 Page
   ├─ 6.3 Lesson
   ├─ 6.4 Assignment แบบมองหมายงานเดี่ยว
   ├─ 6.5 Assignment แบบมอบหมายงานกลุ่ม
   ├─ 6.6 Choice
   ├─ 6.7 Quiz
   └─ 6.8 H5P แบบ Interactive Multimedia
```

---

### **ขั้นตอนที่ 1: Course Settings**

#### **1.1 การตั้งค่าพื้นฐานรายวิชา**

**เป้าหมาย:** กำหนดข้อมูลพื้นฐาน ชื่อวิชา วันเปิด-ปิด

**ขั้นตอน:**

1. **เข้าสู่รายวิชา**
   - Dashboard → My courses → เลือกรายวิชาที่ต้องการ
   
2. **เปิดโหมดแก้ไข**
   - คลิกปุ่ม **"Turn editing on"** มุมขวาบน
   
3. **เข้าสู่การตั้งค่า**
   - คลิกเมนู Settings

4. **ตั้งค่าข้อมูลพื้นฐาน**

**ส่วน General:**
```
Course full name: [ชื่อเต็มรายวิชา]
  ตัวอย่าง: "วิทยาศาสตร์พื้นฐาน สำหรับ ม.4/1 ปีการศึกษา 2569"

Course short name: [ชื่อย่อ - ใช้ในการแสดงผล]
  ตัวอย่าง: "SCI-M4/1-2569"
  หมายเหตุ: ควรมีรหัสวิชา, ระดับชั้น, ห้อง, ปี
  
Course category: [หมวดหมู่วิชา]
  เลือกหมวดหมู่ที่เหมาะสม เช่น "วิทยาศาสตร์", "คณิตศาสตร์"
  (ถ้าไม่มี ใช้ account Admin สร้าง)

Course visibility: Show
  → แสดงรายวิชาให้นักเรียนเห็น

Course start date: [วันที่เปิดเรียน]
  ตัวอย่าง: 1 June 2026

Course end date: [วันที่ปิดเรียน]
  ตัวอย่าง: 31 March 2027
  
Course ID number: [รหัสวิชา (ถ้ามี)]
  ตัวอย่าง: "SCI401-2026"

```
**📌 เทคนิค:**
- ชื่อเต็ม: ใช้ภาษาที่เข้าใจง่าย ระบุระดับชั้น/ห้อง/ปีการศึกษา
- ชื่อย่อ: ใช้รหัสมาตรฐานของสถาบัน สั้นกระชับ
- วันเปิด-ปิด: ตั้งให้ตรงกับปฏิทินการศึกษา → กิจกรรมจะแสดง Relative dates

#### **1.2 การเขียนคำอธิบายรายวิชา (Course Summary)**
Course summary : ข้อมูลสรุปเกี่ยวกับรายวิชา จะแสดงข้อมูลในหน้า Home ของ LMS

Course image : เลือกรูปภาพของรายวิชา รูปภาพจะแสดงในหน้า Home และ My courses 

เขียน Course summary ตามโครงสร้างนี้:

```markdown
🎓 ยินดีต้อนรับสู่รายวิชา [ชื่อวิชา]

## 🎯 โครงสร้างรายวิชา
✨ [หัวข้อหลัก 1]
💻 [หัวข้อหลัก 2]
🎨 [หัวข้อหลัก 3]


## 📊 การประเมินผล
- แบบทดสอบ: XX%
- การบ้าน/Assignment: XX%
- โปรเจกต์: XX%

---
📧 ติดต่อครู: [email]
⏰ เวลาให้คำปรึกษา: [วัน-เวลา]
```
 คลิก **"Save and display"**


#### **1.3 การเลือก Course Format**
**ส่วน Course Format:**

**ตัวเลือกที่ 1: buttons Format (แนะนำสำหรับวิชาที่มีภาพประกอบ)**
```
Course format → เลือก "buttons Format"

ผลลัพธ์: 
หน่วยการเรียนรู้แสดงเป็นปุ่มเมนู คลิกเข้าถึงแต่ละ section ได้
เหมาะกับ: วิชาที่ต้องการ visual ที่น่าสนใจ
```

**ตัวเลือกที่ 2: Collapsed Topics (แนะนำสำหรับวิชาที่มีหลายหน่วย)**
```
Course format → เลือก "Collapsed Topics"

ผลลัพธ์:
หน่วยการเรียนรู้พับได้ คลิกเพื่อขยาย ประหยัดพื้นที่หน้าจอ
เหมาะกับ: วิชาที่มีเนื้อหามาก 8+ หน่วย
```

**ตัวเลือกที่ 3: Weekly sections (แนะนำสำหรับวิชาที่มีตารางเรียนชัดเจน)**
```
Course format → เลือก "Weekly sections"

ผลลัพธ์:
แต่ละ section มีชื่อเป็นช่วงวันที่โดยอัตโนมัติ
เหมาะกับ: วิชาที่มีกำหนดการเรียนตามสัปดาห์
```

**ตัวเลือกที่ 4: Custom sections (Default)**
```
Course format → เลือก "Custom sections"

ผลลัพธ์:
หน่วยการเรียนรู้แบบธรรมดา ตั้งชื่อเองได้อิสระ
เหมาะกับ: ทุกรายวิชา (ยืดหยุ่นที่สุด)
```

5. **บันทึกการตั้งค่า**
   - เลื่อนลงล่างสุด → คลิก **"Save and display"**

---

### **ขั้นตอนที่ 2: Setup Gradebook**

#### **2.1 การทำความเข้าใจ Gradebook**

**สร้างหมวดหมู่คะแนนและกำหนดน้ำหนักให้ถูกต้อง**

**⚠️ ทำไมต้องตั้ง Gradebook ก่อน?**
- เมื่อสร้าง Activity (Quiz, Assignment) จะเลือก Grade category ได้ทันที
- คำนวณคะแนนรวมอัตโนมัติตามน้ำหนักที่กำหนด
- ไม่ต้องกลับมาแก้ไขภายหลัง

**ขั้นตอน:**

1. **เข้าสู่ Gradebook setup**
   - เลือกเมนู → **Grades**
   - ตรงตำแหน่งเมนู **Grader report** ให้เลือกเมนูเป็น → **"Gradebook setup"**

2. **เพิ่ม Grade category**
   
   คลิก **"Add"** แล้วเลือก **"Add category"**
   กำหนดรายละเอียดต่าง ๆ ดังนี้
   
  
**ตัวอย่างโครงสร้าง Gradebook:**
- **หมายเหตุ 1** คลิกเลือก Weight adjusted เพื่อให้มีช่องสำหรับระบุ Weight
- **หมายเหตุ 2** Grade Items จะเพิ่มเติมเข้ามาโดยอัตโนมัติ เมื่อมีการสร้างแบบประเมิน หรือ Assignments ในการทดลอง ให้ทดลองสร้างเองก่อน แต่สามารถแก้ไขภายหลังได้
```
### Course Weights Total (100%)
├─ **Category: แบบทดสอบ** (Weight 30%)
│  ├─ **items: สอบกลางภาค** (Max grade: 20) (คะแนนเต็ม 20)
│  ├─ **items: สอบปลายภาค** (Max grade: 30) (คะแนนเต็ม 30)
├─ **Category: การบ้าน** (Weight 30%)
│  ├─ **items: Assignment 1** (Max grade: 10)
│  ├─ **items: Assignment 2** (Max grade: 10)
│  └─ **items: Assignment 3** (Max grade: 10)
├─ **Category: โปรเจกต์** (30%)
│  └─ **items: Final Project** (Max grade: 30)
└─ **Category: การมีส่วนร่วม** (10%)
   └─ **items: Attendance** (Max grade: 10)
```

---

### **ขั้นตอนที่ 3: Create Groups**

#### **3.1 การสร้างกลุ่มนักเรียน**

**แบ่งนักเรียนเป็นกลุ่ม สำหรับงานกลุ่ม/โปรเจกต์**

**⚠️ ทำไมต้องสร้าง Groups ก่อน?**
- เมื่อสร้าง Assignment จะเลือก "Students submit in groups" ได้
- Forum/Database สามารถตั้งค่า Separate groups ได้
- ง่ายต่อการจัดการและตรวจงานแยกกลุ่ม

**ขั้นตอน:**

1. **เข้าสู่ Groups**
   - เลือกเมนู **"Participants"**
   - เปลี่ยนเมนูด้านซ้ายเดิมจาก **"Enrolled users"** เป็น  **"Groups"**

2. **สร้างกลุ่มแบบ Manual:**
   
   คลิก **"Create group"**
   ```
   Group name: กลุ่มที่ 1
   Group description: [คำอธิบาย ถ้าต้องการ]
   ```
   คลิก **"Save changes"**
   
   เลือกกลุ่ม → คลิก **"Add/remove users"** → เลือกนักเรียน

#### **3.2 การตั้งค่า Group mode**

1. เลือกเมนู **Settings**

2. เมนูย่อย **"Groups"** กำหนดตัวเลือก
   ```
   Group mode: No groups
      (ตั้งเป็น No groups ไว้ก่อน แต่สามารถปรับในแต่ละ Activity ให้เป็นแบบ Group ได้ภายหลัง)
   
   Force group mode: No
      (ให้แต่ละ Activity เลือกได้เอง)
   ```

---

### **ขั้นตอนที่ 4: Organize Sections**

#### **4.1 การสร้างและจัดระเบียบหน่วยการเรียนรู้**

**ตัวอย่างโครงสร้าง:**
```
General (ประกาศ, ช่องทางติดต่อ)

หน่วยที่ 1: (ระบุหัวข้อ)
├─ [Description บอกว่าเรียนอะไร]

หน่วยที่ 2: (ระบุหัวข้อ)
├─ [Description บอกว่าเรียนอะไร]

หน่วยที่ 3: (ระบุหัวข้อ)
├─ [Description บอกว่าเรียนอะไร]
```
**แก้ไขโดยเลือก เมนูจุดสามจุด (Tree dot)ของ Sections ที่ต้องการ แล้วเลือก Edit settings**
---

### **ขั้นตอนที่ 5: Prepare Resources**
#### **5.1 Page - เอกสารออนไลน์**

**📝 โจทย์:** สร้างเอกสารเนื้อหาออนไลน์สำหรับหน่วยที่ 1

**🎯 ข้อกำหนดที่ต้องทำ:**
1. เขียนเนื้อหาอย่างน้อย 3 ย่อหน้า
2. มีหัวข้อย่อย (Headings) อย่างน้อย 3 หัวข้อ
3. แทรกรูปภาพ 1 รูป
4. ไม่ให้คะแนน แต่ต้องติดตามว่าอ่านแล้ว (Activity completion)
5. กำหนด Expect completed on เป็นวันก่อนสอบ
6. ใช้เป็นเงื่อนไขปลดล็อก Lesson

**ขั้นตอน:**

1. **Add an activity or resource** → **"Page"**

2. **ตั้งค่าพื้นฐาน:**
```
Name: 📖 บทที่ 1: [ชื่อหัวข้อของคุณ]
   ตัวอย่าง: "บทที่ 1: โครงสร้างอะตอม"

Description: [เว้นว่าง]
☐ Display description on course page: No
```

3. **Page content:** เขียนตามโครงสร้างนี้

```markdown
# บทที่ 1: [ชื่อหัวข้อ]

## 🎯 วัตถุประสงค์
เมื่อจบบทนี้ นักศึกษาสามารถ:
- [วัตถุประสงค์ 1]
- [วัตถุประสงค์ 2]
- [วัตถุประสงค์ 3]

---

## 📚 เนื้อหา

### 1.1 [หัวข้อย่อยที่ 1]
[เขียนเนื้อหาอย่างน้อย 1 ย่อหน้า]

### 1.2 [หัวข้อย่อยที่ 2]
[เขียนเนื้อหาอย่างน้อย 1 ย่อหน้า]

[**แทรกรูปภาพตรงนี้**]

### 1.3 [หัวข้อย่อยที่ 3]
[เขียนเนื้อหาอย่างน้อย 1 ย่อหน้า]

---

## 📝 สรุป
[สรุปสั้นๆ]
```

4. **การแทรกรูปภาพ:**

ในตัวแก้ไขข้อความ:
- คลิกปุ่ม **"Insert → Image"** (🖼️)
- **Upload a file** → เลือกรูปจากเครื่อง

5. **⭐ Completion conditions:**
```
 Add requirements: View the activity
 Set reminder in Timeline: กำหนดวันที่แจ้งเตือนนักศึกษา

```
6. **บันทึก** → **"Save and display"**

#### **5.2 การเพิ่ม File (อัพโหลดไฟล์)**

**เป้าหมาย:** อัพโหลด PDF, PowerPoint, เอกสารให้นักเรียนดาวน์โหลด

**ขั้นตอน:**

1. **Add an activity or resource** → เลือก **"File"**

2. **ตั้งค่า:**
   ```
   Name: 📄 เอกสารประกอบ: เรื่อง (ระบุเรื่อง)
   
   Description:
   "ระบุหัวข้อเรื่อง พร้อมคำอธิบาย"
   ☑ Display description on course page: Yes
   ```

3. **Select files**
   
   คลิก **"Add"** → เลือก **"Upload a file"**
   
   เลือกไฟล์จากเครื่อง → **"Upload this file"**

   ```

4. **Completion conditions:**
   ```
     Students must manually mark the activity as done
   ```

5. คลิก **"Save and display"**


#### **5.3 การเพิ่ม URL (ลิงก์ภายนอก)**

**เป้าหมาย:** ลิงก์ไปยังวิดีโอ YouTube, เว็บไซต์ภายนอก

**ขั้นตอน:**

1. **Add an activity or resource** → เลือก **"URL"**

2. **ตั้งค่า:**
   ```
   Name: 📹 วิดีโอ: (ระบุเรื่อง ระบุแหล่งที่มา)
   
   Description:
   "ดูวิดีโอเพื่อทบทวนเนื้อหา (10 นาที)"
   ☑ Display description on course page: Yes
   
   External URL: [วาง URL เช่น https://www.youtube.com/watch?v=XXXXX]
   ```

3. **Appearance:**
   ```
   Display: Automatic (Moodle เลือกให้อัตโนมัติ)
   หรือ
   Display: Embed (ฝังวิดีโอในหน้า Moodle เลย)
   ```

4.**Completion conditions:**
```
  เลือก Add requirements :  
      เลือก View the activity
```

5. คลิก **"Save and display"**

---

#### **5.4 Lesson - บทเรียนแบบมีเงื่อนไข**

**📝 โจทย์:** สร้างบทเรียนแบบมีการแบ่งหน้าและคำถามคั่นระหว่างเรียน

**🎯 ข้อกำหนดที่ต้องทำ:**
1. มี Content pages อย่างน้อย 3 หน้า
2. มี Question pages (Multiple choice) อย่างน้อย 2 ข้อ
3. ตอบผิด → กลับไปอ่านหน้าเดิม (This page)
4. ตอบถูก → ไปหน้าถัดไป (Next page)
5. ให้คะแนนในหมวด "การมีส่วนร่วม" 5 คะแนน
6. ล็อกไว้ ต้องอ่าน Page ก่อนถึงจะเข้าได้
7. เปิด Progress bar และ Display menu

**ขั้นตอน:**

1. **Add an activity or resource** → **"Lesson"**

2. **ตั้งค่าพื้นฐาน:**
```
Name: 📘 บทเรียน: [หัวข้อ]
Description:
"บทเรียนมี 3 หน้า และคำถามทดสอบความเข้าใจ 2 ข้อ
📖 อ่านอย่างละเอียด
✅ ตอบคำถามให้ถูกต้อง"

☑ Display description on course page: Yes
```

3. **Appearance:**
```
☑ Progress bar: Yes
☑ Display menu: Yes

```

4. **⭐ Grade:**
```
Grade category: การมีส่วนร่วม
Type: Point
Maximum grade: 5
Grade to pass: 3 (60%)
```

5. **⭐ Restrict access:**
```
Add restriction...
   Activity completion
   Activity: "📖 บทที่ 1: [ชื่อ]" (Page ที่สร้างไว้)
   must be marked complete

คลิกไอคอน 👁️ → เลือก "Shown" (แสดงแต่ล็อก)
```

6. **⭐ Completion conditions:**
```
   ☑ Add requirements: ☑ Received a grade ☑ Passing grade
```

7. **บันทึก** → **"Save and display"**

8. **สร้างเนื้อหา Lesson:**

คลิก **"Add a content page"**

```
Page title: (ระบุ title)

Page contents:
[เขียนเนื้อหา 1-2 ย่อหน้า เกี่ยวกับหัวข้อที่สอน]

---

Content 1:
Description: ▶️ ต่อไป
Jump: Next page
```

คลิก **"Save page"**

**หน้าที่ 2: Question page (คำถามที่ 1)**

คลิก **"Add a question page"** → เลือก **"Multiple choice"**

```
Page title: ❓ คำถามที่ 1

Page contents:
"ระบุข้อคำถาม?"

Answer 1: (ตัวเลือกที่ 1) ✓
   Response: (ข้อความแสดง ถ้าตอบตัวเลือกนี้)
   Jump: Next page
   Score: 1
   
Answer 2: (ตัวเลือกที่ 2)
   Response: ❌ ไม่ถูกต้อง ลองอ่านใหม่อีกครั้ง
   Jump: This page (ให้ทำใหม่)
   Score: 0

Answer 3: (ตัวเลือกที่ 3)
   Response: ❌ ไม่ถูกต้อง ลองอ่านใหม่อีกครั้ง
   Jump: This page
   Score: 0

Answer 4: (ตัวเลือกที่ 4)
   Response: ❌ ไม่ถูกต้อง ลองอ่านใหม่อีกครั้ง
   Jump: This page
   Score: 0
```

คลิก **"Save page"**

**หน้าที่ 3: Content page**

คลิก **"Add a content page"**

```
Page title: (ระบุ)

Page contents:
[เขียนเนื้อหาต่อ 1-2 ย่อหน้า]

---

Content 1:
Description: ▶️ ต่อไป
Jump: Next page
```

**หน้าที่ 4: Question page (คำถามที่ 2)**

คลิก **"Add a question page"** → **"Multiple choice"**

```
Page title: ❓ คำถามที่ 2

Page contents:
[ถามคำถามเกี่ยวกับเนื้อหาที่สอน]

[สร้างคำตอบ 3-4 ข้อ โดย:
- คำตอบถูก: Jump = Next page, Score = 1
- คำตอบผิด: Jump = This page, Score = 0]
```

**หน้าที่ 5: Content page (สรุป)**

คลิก **"Add a content page"**

```
Page title: 🎉 สรุป

Page contents:
"ยินดีด้วย! คุณจบบทเรียนแล้ว

---

Content 1:
Description: ✅ จบบทเรียน
Jump: End of lesson
```
---

#### **5.5 Assignment (งานเดี่ยว)**

**📝 โจทย์:** สร้าง Assignment สำหรับส่งงานรายบุคคล

**🎯 ข้อกำหนดที่ต้องทำ:**
1. ให้ส่งไฟล์ PDF เท่านั้น (ไม่รับ .doc, .txt)
2. ส่งได้ 1 ไฟล์ ขนาดไม่เกิน 10 MB
3. กำหนดส่ง (Due date) และวันปิดรับ (Cut-off) ห่างกัน 2 วัน
4. เตือนครูให้ตรวจ 5 วันหลัง Due date
5. ให้คะแนนในหมวด "การบ้าน" 10 คะแนน
6. เกรดผ่าน = 7 (70%)
7. ใช้ Annotate PDF เป็น Feedback
8. ล็อกไว้ ต้องทำ Lesson ให้ผ่านก่อน

**ขั้นตอน:**

1. **Add an activity or resource** → **"Assignment"**

2. **ตั้งค่าพื้นฐาน:**
```
Assignment name: 📝 งานที่ 1: สรุป[หัวข้อ]
Description:(ระบุข้อความสั้น ๆ)
   ☑ Display description on course page: Yes
Activity instructions:
"📄 จัดทำเอกสารสรุป 2-3 หน้า

เนื้อหาที่ต้องมี:
1. ความเป็นมา
2. แนวคิดหลัก
3. ตัวอย่างการประยุกต์ใช้
4. บทสรุป

📎 ส่งเป็น PDF เท่านั้น
📏 ความยาว 2-3 หน้า A4
🔤 ฟอนต์ TH Sarabun, ขนาด 16

📅 กำหนดส่ง: [วันที่] 23:59 น."

```

3. **Availability:**
```
Allow submissions from: [วันนี้หรือวันที่เหมาะสม]
Due date: [วันที่กำหนดส่ง] 23:59
Cut-off date: [Due date + 2 วัน] 23:59
Remind me to grade by: [Due date + 5 วัน] 09:00
☑ Always show description: Yes
```

4. **Submission types:**
```
☐ Online text: No

☑ File submissions: Yes
   Maximum number of uploaded files: 1
   Maximum submission size: 10 MB
   Accepted file types: .pdf
```

5. **Feedback types:**
```
☑ Feedback comments: Yes
☑ Annotate PDF: Yes
☐ Offline grading worksheet: No
☐ Feedback files: No
☐ Comment inline: No
```

6. **Submission settings:**
```
☑ Require students click submit button: Yes
☑ Require that students accept the submission statement: Yes
Allowed attempts: 2
```

7. **⭐ Grade:**
```
Grade:
   Type: Point
   Maximum grade: 10
   Grading method: Simple direct grading
   Grade category: การบ้าน

Grade to pass: 7 (70%)
```

8. **⭐ Restrict access:**
```
Add restriction...
   Activity completion
   Activity: "📘 บทเรียน: [ชื่อ]" (Lesson ที่สร้างไว้)
   must be complete with pass grade

คลิกไอคอน 👁️ → "Shown"
```

9. **⭐ Completion condition:**
```
☑ Add requirements: ☑ Make a submission
☑ Set reminder in Timeline : ☑ Enable (ระบุวันแจ้งเตือน)
```

10. **บันทึก** → **"Save and display"**

---

#### **5.6 Assignment (งานกลุ่ม)**

**📝 โจทย์:** สร้าง Assignment สำหรับส่งงานกลุ่ม

**🎯 ข้อกำหนดที่ต้องทำ:**
1. แต่ละกลุ่มส่งงานร่วมกัน (Group submission)
2. สมาชิกคนใดคนหนึ่งส่งแทนกลุ่มได้ (ไม่ต้องส่งทุกคน)
3. ส่งได้ 2 ไฟล์ (.pdf, .pptx)
4. ขนาดไม่เกิน 20 MB
5. ให้คะแนนในหมวด "โปรเจกต์" 30 คะแนน
6. เกรดผ่าน = 21 (70%)
7. ให้ Feedback เป็น Comments + Files
8. ไม่มี Restrict access (เข้าได้เลย)

**ขั้นตอน:**

1. **Add an activity or resource** → **"Assignment"**

2. **ตั้งค่าพื้นฐาน:**
```
Description: (ระบุ)
   ☑ Display description on course page: Yes
Activity instructions:
Assignment name: 🎯 โปรเจกต์กลุ่ม: [หัวข้อ]
Description:
"📊 ทำโปรเจกต์เป็นกลุ่ม

ส่งมา 2 ไฟล์:
1. รายงาน (PDF)
2. สไลด์นำเสนอ (PPTX)

👥 สมาชิกในกลุ่มคนใดคนหนึ่งส่งแทนทั้งกลุ่มได้
🏆 ทุกคนในกลุ่มได้คะแนนเท่ากัน

📅 กำหนดส่ง: [วันที่] 23:59 น."


```

3. **Availability:**
```
Allow submissions from: [วันที่เหมาะสม]
Due date: [วันที่กำหนดส่ง] 23:59
Cut-off date: [Due + 3 วัน] 23:59
Remind me to grade by: [Due + 7 วัน] 09:00
```

4. **Submission types:**
```
☐ Online text: No

☑ File submissions: Yes
   Maximum number of uploaded files: 2
   Maximum submission size: 20 MB
   Accepted file types: .pdf, .pptx
```

5. **Feedback types:**
```
☑ Feedback comments: Yes
☐ Annotate PDF: No
☐ Offline grading worksheet: No
☑ Feedback files: Yes (ส่งไฟล์กลับได้)
☐ Comment inline: No
```

6. **⭐ Group submission settings:**
```
☑ Students submit in groups: Yes

☐ Require all group members submit: No
   (คนใดคนหนึ่งส่งแทนกลุ่มได้)

☐ Grouping for student groups: [None]
```

7. **⭐ Grade:**
```
Grade:
   Type: Point
   Maximum grade: 30
   Grading method: Simple direct grading
   Grade category: โปรเจกต์

Grade to pass: 21 (70%)
```

8. **⭐ Restrict access:**
```
(ไม่ตั้ง - ให้เข้าได้เลย)
```

9. **⭐ Completion conditions:**
```
☑ View the activity
☑ Make a submission
Expect completed on: [Due date]
```

10. **บันทึก** → **"Save and display"**

---

#### **5.7 Choice - การโหวต/เลือก**

**📝 โจทย์:** สร้าง Choice ให้นักเรียนเลือกหัวข้อที่สนใจ

**🎯 ข้อกำหนดที่ต้องทำ:**
1. มี 3 ตัวเลือก จำกัดคนที่เลือกได้ตัวเลือกละ 10 คน
2. เลือกแล้วห้ามเปลี่ยนใจ (Allow update = No)
3. แสดงผลลัพธ์หลังตอบ (After they answer)
4. ไม่ให้คะแนน
5. ตั้งค่า Activity completion เป็น Manual
6. ไม่มี Restrict access

**ขั้นตอน:**

1. **Add an activity or resource** → **"Choice"**

2. **ตั้งค่าพื้นฐาน:**
```
Choice name: 🗳️ เลือกหัวข้อที่สนใจ

Description:
"กรุณาเลือกหัวข้อที่คุณสนใจ
ระบบจะใช้ข้อมูลนี้ในการจัดกลุ่มโปรเจกต์

⚠️ เลือกแล้วไม่สามารถเปลี่ยนแปลงได้
📊 แต่ละหัวข้อจำกัด 10 คนเท่านั้น"

☑ Display description on course page: Yes
```

3. **ตั้งค่าตัวเลือก (Options):**
  - Allow choice to be updated: No (ห้ามเปลี่ยนใจ)
  - Allow more than one choice to be selected: No (ให้เลือกได้ 1 ตัวเลือกเท่านั้น)
  - Limit the number of responses allowed: Yes
**Option 1:**
```
Choice 1: 🛒 หัวข้อที่ 1: [ชื่อหัวข้อ]
Limit: 10

```

**Option 2:**
```
Choice 2: ✈️ หัวข้อที่ 2: [ชื่อหัวข้อ]
Limit: 10
```

**Option 3:**
```
Choice 3: 📚 หัวข้อที่ 3: [ชื่อหัวข้อ]
Limit: 10
```

4. **Availability:**
```
Allow responses from: [วันที่เปิด]
Allow responses until: [วันที่ปิด]
```

5. **ตั้งค่าผลลัพธ์:**
```

Publish results: Show results to students after they answer

Privacy of results: Publish full results, showing names and their choices

☑ Show column for unanswered: Yes
```

6. **⭐ Completion conditions:**
```
   Students must manually mark the activity as done
```

7. **บันทึก** → **"Save and display"**

---

#### **6.7 Quiz - แบบทดสอบ (30 นาที)**

**📝 โจทย์:** สร้าง Quiz แบบสุ่มคำถาม

**🎯 ข้อกำหนดที่ต้องทำ:**
1. สุ่มคำถาม 10 ข้อ จาก Question Bank ที่สร้างไว้
2. เวลา 15 นาที หมดเวลาส่งอัตโนมัติ
3. ทำได้ 2 ครั้ง เก็บคะแนนสูงสุด
4. สุ่มลำดับคำถามและตัวเลือก
5. ให้คะแนนในหมวด "แบบทดสอบ" 10 คะแนน
6. เกรดผ่าน = 7 (70%)
7. แสดง Feedback หลังส่งข้อสอบ
8. ล็อกไว้ ต้องทำ Assignment (งานเดี่ยว) ส่งก่อน

**ขั้นตอน:**

1. **Add an activity or resource** → **"Quiz"**

2. **ตั้งค่าพื้นฐาน:**
```
Name: ✏️ แบบทดสอบบทที่ 1

Description:
"📝 แบบทดสอบ 10 ข้อ คะแนนเต็ม 10
⏰ เวลา 15 นาที
🔄 ทำได้ 2 ครั้ง (เก็บคะแนนสูงสุด)
🎲 คำถามสุ่มจาก Question Bank

เกณฑ์ผ่าน: 70% (7 คะแนน)"

☑ Display description on course page: Yes
```

3. **Timing:**
```
Open the quiz: [วันที่เปิด]
Close the quiz: [วันที่ปิด]

☑ Time limit: 15 minutes
   When time expires: There is a grace period when open attempts can be Submited, but no more questions answered (มีช่วงเวลาผ่อนผันให้ส่งคำตอบที่ทำค้างไว้ได้ แต่จะไม่สามารถตอบคำถามเพิ่มเติมได้แล้ว)
   
Submission grace period: 60 seconds
```

4. **⭐ Grade:**
```
Grade category: แบบทดสอบ

Attempts allowed: 2
Grading method: Highest grade
Grade to pass: 7
```

5. **Layout:**
```
New page: Every question (แยกหน้าทีละข้อ)
Navigation method: Free (ข้ามไปมาได้)
```

6. **Question behaviour:**
```
☑ Shuffle within questions: Yes (สุ่มตัวเลือก)

How questions behave: Deferred feedback
   (ดูผลหลังส่งข้อสอบทั้งหมด)
Each attempt builds on the last: No
```
| ตัวเลือก (Behavior) | เห็นคะแนนเมื่อไหร่? | แก้ตัวในข้อเดิมได้ไหม? | เหมาะกับงานประเภทใด |
| :--- | :--- | :--- | :--- |
| **Deferred feedback** | หลังส่งข้อสอบทั้งชุด | **ไม่ได้** | สอบกลางภาค / ปลายภาค (เน้นความปลอดภัย) |
| **Interactive with multiple tries** | หลังกดตรวจทีละข้อ | **ได้** (มักมีการหักคะแนนสะสม) | แบบฝึกหัดเตรียมสอบ / เน้นการเรียนรู้ |
| **Immediate feedback** | หลังกดตรวจทีละข้อ | **ไม่ได้** | ทดสอบความรู้สั้นๆ ที่ต้องการให้รู้ผลทันที |
| **Adaptive mode** | ทันทีที่กดส่งข้อนั้น | **ได้** (ตอบจนกว่าจะถูก) | การเรียนรู้ด้วยตนเอง / ฝึกทักษะเฉพาะทาง |


7. **Review options:**
```
During the attempt:
   [ไม่ต้องเลือก อะไร] (ป้องกันโกง)

Immediately after the attempt:
   ☑ The attempt
   ☑ Whether correct
   ☑ Marks
   ☑ Specific feedback
   ☐ General feedback
   ☐ Right answer (ยังไม่บอก - ให้ทำซ้ำได้)

Later, while the quiz is still open:
   [เลือกเหมือน Immediately]

After the quiz is closed:
   ☑ [ติกทุกอัน] (แสดงทุกอย่างหลังปิดสอบ)
```

8. **⭐ Restrict access:**
```
Add restriction...
   Activity completion
   Activity: "📝 งานที่ 1: สรุป[หัวข้อ]" (Assignment งานเดี่ยว)
   must be marked complete

คลิกไอคอน 👁️ → "Shown"
```

9. **⭐ Completion conditions:**
```
☑ Add requirements 
☑ View the activity
☑ Receive a grade: Passing grade

```

10. **บันทึก** → **"Save and display"**

11. **เพิ่มคำถาม:**

คลิก **"Add"** ที่อยู่ด้านขวา → เลือก **"a new question"**

```
เลือกรูปแบบข้อสอบ Multiple choice และ True false รวมกัน 5 ข้อ
```

### รูปแบบข้อสอบแบบต่าง ๆ อยู่ในใบงานการทดลองถัดไป 
### การตรวจใบงานการทดลอง จะเป็นแบบ Peer assessment (ให้เพื่อนตรวจใบงานว่าทำครบถ้วนหรือไม่)

