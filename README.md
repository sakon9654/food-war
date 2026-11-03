# FOOD WAR — Novel Writing Vault

นิยายเอาชีวิตรอด / ทำอาหาร / ความสัมพันธ์ / โลกหลังหายนะ · เก็บ **Canon + ตอนนิยาย + ระบบวางแผนและตรวจความต่อเนื่อง** เป็น Markdown บน GitHub เพื่อใช้ร่วมกับ Obsidian และ ChatGPT

> **สถานะล่าสุด:** เล่ม 1 เผยแพร่ตอน 1–11; ผู้เขียน Approve ถึงตอน 10. ดู [ดัชนีตอน](Chapters/Volume-01/Chapter-Index.md) ก่อนเขียนต่อ

## เริ่มใช้งาน

| ถ้าต้องการ... | เปิดไฟล์ |
|---|---|
| หน้า Home ใน Obsidian | [00-Home.md](00-Home.md) |
| อ่านนิยายตามลำดับ | [Chapter Index](Chapters/Volume-01/Chapter-Index.md) |
| ตรวจเส้นเวลา | [Timeline](Story/Timeline.md) |
| ดูปมที่ยังไม่เฉลย | [Plot Threads](Story/Plot-Threads.md) |
| รู้ว่าตัวละครอยู่ในสภาพไหน | [Character Index](Characters/Character-Index.md) |
| ตรวจสถานที่และเขตเสี่ยง | [Location Index](Locations/Location-Index.md) |
| ตรวจพลังและข้อจำกัด | [Power Index](Systems/Power-Index.md) |
| อ่านกฎโลก | [World Bible](Bible/World-Bible.md) |
| อ่านกฎพลัง | [Survival Power Bible](Bible/Survival-Power-Bible.md) |
| ตรวจสิ่งที่ *ยังไม่เกิด* ในเรื่อง | [Future Arc Plan](Story/Future-Arc-Plan.md) |
| เริ่มงานใน ChatGPT จากบริบทเดียวกัน | [AI Session Brief](Workflow/AI-Session-Brief.md) |
| ดูวิธีทำงานใน Obsidian/ChatGPT/GitHub | [Workflow](Workflow/ChatGPT-Obsidian-Workflow.md) |
| ตรวจความต่อเนื่องก่อน Commit | [Continuity Checklist](Workflow/Continuity-Checklist.md) |

## โครงสร้างโฟลเดอร์

```text
food-war/
├── 00-Home.md                # หน้าเริ่มต้น Obsidian
├── Chapters/
│   └── Volume-01/
│       ├── Chapter-Index.md # สารบัญและสถานะ Approve
│       └── Chapter-01..11.md
├── Bible/                    # กฎ CANON ที่ต้องรักษา
├── Characters/               # รายละเอียดตัวละคร/ความสัมพันธ์
├── Locations/                # สถานที่ เขตเสี่ยง เส้นทาง
├── Systems/                  # ดัชนีพลัง/กลไก
├── Story/                    # Timeline, Plot Threads, แผน, สมุดอาหาร
├── Workflow/                 # AI brief, checklist, decision log, series roadmap
├── Templates/                # แม่แบบแฟ้มตัวละครและโน้ตตอน
├── .obsidian/                # การตั้งค่าทั่วไป ไม่ใส่ workspace ส่วนตัว
└── .gitignore
```

## ทำงานใน Obsidian
1. Clone Repo: `git clone https://github.com/sakon9654/food-war.git`
2. Obsidian → **Open folder as vault** → เลือก `food-war`
3. เปิด `00-Home.md`; คลิก Wikilinks `[[...]]` แล้วใช้ Graph, Backlinks, Outgoing Links และ Search
4. แก้ไฟล์ → Commit/Push กลับ GitHub ก่อนให้ ChatGPT ดำเนินเรื่องต่อ เพื่อหลีกเลี่ยงข้อมูลคนละเวอร์ชัน

**หมายเหตุ:** Obsidian Wikilinks ใช้งานใน Obsidian; ลิงก์ใน README นี้เป็น Markdown ปกติเพื่อเปิดบน GitHub ได้โดยตรง. ไม่มีการตั้งค่า Sync อัตโนมัติหรือ GitHub token อยู่ใน Repository. Obsidian ใช้งานไฟล์หลักได้โดยไม่ต้องลง Community Plugin.

## กติกาการเขียนระยะยาว
- แยก **FACT** (เกิดในตอนที่เผยแพร่แล้ว), **CANON** (กฎที่อนุมัติ), **PLANNED** (แผนในอนาคต), และ **OPEN** (ยังไม่เฉลย)
- ต้นฉบับที่อนุมัติแล้วไม่แก้เงียบๆ; ใช้ Git History บันทึกทุกครั้งที่ปรับ
- ใช้ภาษาไทยร่วมสมัย **ไม่ใช้ “ข้า–เจ้า”** และบทสนทนาต้องมีจังหวะเหมือนคนคุยจริง ดู [World Bible](Bible/World-Bible.md)
- เงื่อนไขพลัง อาหาร การเจ็บป่วย การถนอมอาหาร และการค้นพบพลังต้องเป็นไปตาม [Survival Power Bible](Bible/Survival-Power-Bible.md)
- หลังเผยแพร่ตอนใหม่ ต้องปรับ [Chapter Index](Chapters/Volume-01/Chapter-Index.md), [Timeline](Story/Timeline.md), [Plot Threads](Story/Plot-Threads.md), แฟ้มตัวละครและสถานที่ที่ได้รับผล
- ดู [Decision Log](Workflow/Decision-Log.md) เพื่อไม่เปลี่ยนข้อตกลงเก่าโดยไม่รู้ตัว

## สำหรับ ChatGPT
ก่อนเขียนหรือแก้ไขให้เริ่มจาก [AI Session Brief](Workflow/AI-Session-Brief.md) + ตอนล่าสุด + [Continuity Checklist](Workflow/Continuity-Checklist.md). ต้องอ้างอิง Repo ปัจจุบันแทนความจำเดิม และรายงานลิงก์ Commit ที่สำเร็จจริง
