---
type: workflow
tags: [workflow, chatgpt, obsidian, github]
---
# วิธีทำงานร่วมกัน: ChatGPT ↔ GitHub ↔ Obsidian

[[00-Home|หน้าหลัก]] · [[Workflow/Continuity-Checklist|รายการตรวจ]] · [[Chapters/Volume-01/Chapter-Index|สารบัญ]] · [[Series/Series-Index|ระบบหลายเล่ม]]

## หน้าที่ของแต่ละระบบ
- **GitHub (main)** = แหล่งไฟล์จริง (source of truth) เก็บต้นฉบับและ Canon พร้อมประวัติ Commit
- **Obsidian** = อ่าน/แก้ Markdown ภายในโฟลเดอร์ Repository ใช้ Graph View, Backlinks, Search, Properties, Templates และลิงก์ระหว่างไฟล์
- **ChatGPT** = ช่วยเขียน ตรวจความต่อเนื่อง และอัปเดตไฟล์ GitHub ตามคำสั่ง ไม่ใช่ฐานข้อมูลเงาที่แทน Repo

## เปิด Vault ครั้งแรก
1. Clone `https://github.com/sakon9654/food-war.git` หรือดาวน์โหลด ZIP แล้วแตกไฟล์ (Clone เหมาะกว่าเพราะ Sync กลับ GitHub ได้)
2. เปิด Obsidian → **Open folder as vault** → เลือกโฟลเดอร์ `food-war`
3. เปิด [[00-Home]] และใช้ `Ctrl/Cmd+O` ค้นชื่อแฟ้ม; Graph View / Backlinks ดูความเชื่อมโยง
4. Obsidian เปิด Markdown ได้โดยไม่ต้องติดตั้ง Plugin ใดๆ; .obsidian ที่ติดตามใน Repo เก็บค่าทั่วไป **ไม่เก็บหน้าต่าง workspace ส่วนบุคคล**
5. ถ้าแก้บนคอม ให้ **Commit + Push** ก่อนขอ ChatGPT เขียนต่อ เพื่อไม่ให้เขียนบนข้อมูลเก่า

## วงรอบการเขียนหนึ่งตอน
**ก่อนเขียน:** ตรวจ `main` ล่าสุด → อ่าน [[Bible/World-Bible]], [[Bible/Survival-Power-Bible]], [[Story/Timeline]], [[Story/Plot-Threads]], [[Series/World-State]], Tracker ข้ามเล่มที่เกี่ยวข้อง, แฟ้มตัวละคร/สถานที่ และตอนล่าสุด

**ระหว่างเขียน:** เขียน `Chapters/Volume-01/Chapter-XX.md`; ใช้ภาษาไทยร่วมสมัย/บทสนทนาธรรมชาติ; ไม่ใส่สปอยล์แผนอนาคตในบทที่ยังไม่ถึง; ให้สิ่งที่ตัวละครรู้สัมพันธ์กับเหตุการณ์ที่เห็น

**หลังเขียน:** ตรวจตาม [[Workflow/Continuity-Checklist]] → Commit ต้นฉบับ → อัปเดต Chapter Index/Timeline/Plot Threads/แฟ้มที่เกี่ยวข้อง รวมถึง [[Series/Series-Timeline]], [[Series/Arc-Tracker]], [[Series/Character-Progression]], [[Series/World-State]] หรือ [[Series/Foreshadowing-Tracker]] เฉพาะที่ได้รับผล → Commit สรุปต่อเนื่อง หรือ Commit ร่วมกันหากทำเป็นชุดเดียว → แจ้งลิงก์ตอนในแชตแบบสั้น

**เมื่อผู้เขียน Approve:** เปลี่ยน `approved_through` ในดัชนี ห้ามปรับย้อนหลังโดยไม่มีคำสั่ง; หากต้องรีไรต์ให้แยก Commit อธิบายสิ่งที่เปลี่ยน

## เปลี่ยนผ่านระหว่างเล่ม

1. อย่าสร้างผลลัพธ์ของเล่มถัดไปจาก [[Story/Future-Arc-Plan]]; เอกสารนั้นเป็น PLANNED จนมีตอนเผยแพร่รองรับ
2. เมื่อผู้เขียนยืนยันปิดเล่ม ให้สร้าง/ปิด [[Series/Volume-Handoffs/Volume-01-Handoff|Volume Handoff]] จาก [[Templates/Volume-Handoff-Template]] และตรวจ Tracker ทั้งห้าชุด
3. ย้ายเฉพาะปม `OPEN` และสถานะ FACT ล่าสุดไปเป็นบริบทเริ่มเล่มใหม่; เก็บ CANON แยกจากความรู้ของตัวละคร
4. สร้าง `Chapters/Volume-02/Chapter-Index.md` และตอนใหม่หลัง Gate ใน Handoff ผ่านแล้ว ใช้ Wikilink เต็มเพื่อป้องกันชื่อ `Chapter-01` ซ้ำกัน

## ตัวอย่างคำสั่งให้ ChatGPT ใช้กับ Repo นี้
- “Approve ตอน 11 แล้วเขียนตอน 12; ตรวจ Timeline/Plot-Threads/Canon ก่อน Commit”
- “แก้บทสนทนาตอน 9 ให้เหมือนคนพูดจริง ไม่แก้ลำดับเหตุการณ์ แล้วอัปเดตบันทึกความต่อเนื่อง”
- “ทำรายงานสิ่งที่อีธานรู้จริงถึงตอน 11 เทียบกับสิ่งที่ผู้อ่านรู้”
- “สรุปปมที่ยังไม่เฉลยจาก T01–T06 โดยไม่แต่งคำตอบ”
- “ตรวจลิงก์และสถานะ APPROVED ของ Vault ก่อนเริ่มเล่ม 2”

## หมายเหตุเรื่อง Sync และความปลอดภัย
- GitHub ไม่อัปเดต Obsidian ในเครื่องเอง และการแก้ใน Obsidian ก็ไม่ส่ง GitHub เอง; ต้องใช้ Git (หรือ Plugin Sync ที่ผู้ใช้ติดตั้งและตั้งค่า) เพื่อดึง/ส่งไฟล์
- หลีกเลี่ยงไฟล์ลับ รหัสผ่าน Token และ workspace อุปกรณ์ส่วนตัวใน Repo
- หากแก้พร้อมกันบน Obsidian และ ChatGPT อาจเกิด merge conflict; Pull ล่าสุดก่อนทำงานทุกครั้ง
- Obsidian Wikilink มักแสดงบน GitHub เป็นข้อความ `[[...]]`; ให้ใช้ Obsidian สำหรับเดินลิงก์ภายใน
