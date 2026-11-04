# Once Human — Fusion Pod Planner

หน้าเว็บช่วยวางแผนการผสม Deviation ใน Fusion Pod ของเกม Once Human

เลือก Deviation, Variant และ Trait ที่ต้องการ แล้วหน้าเว็บจะวางลำดับการผสมให้ทีละขั้น (เก็บ trait ลงตัวพา → รวม trait → โคลน → ย้ายเข้าเป้าหมาย → ไล่ค่า x/5 → 5/5) พร้อมคำนวณโอกาสของแต่ละขั้น

## วิธีใช้

เปิดไฟล์ `index.html` ในเบราว์เซอร์ได้เลย ไม่ต้องติดตั้งอะไร หรือเปิดผ่าน GitHub Pages

มี 4 แท็บ:

- **วางแผนการผสม** — เลือกเป้าหมาย แล้วดูขั้นตอนพร้อมวิธีจัดวางในเครื่องและโอกาสสำเร็จ
- **เครื่องจำลอง Fusion Pod** — จัดหลอดซ้าย/ขวาและวัสดุ 3 ช่องเอง แล้วดูโอกาสของสายพันธุ์ trait และค่า Skill/Activity
- **รายการ Trait** — ค้นหาและกรอง trait ตามช่องและประเภท
- **ตั้งค่าและกฎ** — ปรับตัวเลขที่ใช้คำนวณ

## กฎที่ใช้คำนวณ

1. สายพันธุ์ลูกได้เฉพาะสายพันธุ์ของพ่อหรือแม่ โอกาส = จำนวนตัวสายพันธุ์นั้น (พ่อแม่ + วัสดุ) ÷ จำนวนตัวที่เป็นสายพันธุ์ของพ่อแม่ทั้งหมด
2. Trait มี 4 ช่อง: ทั่วไป, ประจำสาย, Deviated, Stat (SCP) ลูกได้ช่องละไม่เกิน 1
3. Variant เฉพาะตัว (เช่น Starry Night ของ Butterfly, Golden ของ Eel) ใช้ช่องประจำสายเป็นค่าเริ่มต้น จึงล็อกได้สูงสุด 4 trait (ทั่วไป + Variant + Deviated + Stat SCP) เปลี่ยนเป็นช่องทั่วไปได้ในแท็บตั้งค่า ถ้าลูกไม่ใช่สายพันธุ์นั้นช่องจะว่าง
4. Trait ประจำสายข้ามสายไม่ได้
5. หลาย trait แย่งช่อง: โอกาส = จำนวนแหล่งของ trait ÷ จำนวนแหล่งทั้งหมดในช่อง
6. Trait เดียวในช่อง: 2 แหล่งขึ้นไป = 100% แหล่งเดียว = 50% + 10% ต่อ Deviation ที่ไม่มี trait ในช่องนั้น (สูงสุด 80%)
7. ค่า Skill/Activity สุ่มจากพ่อหรือแม่ แล้วมีโอกาส +1 (~9.8%) หรือ −1 (~2%)

ตัวเลขเป็นค่าประมาณจากผู้เล่น ยังไม่ยืนยันจากผู้พัฒนา ให้เทียบกับหน้า preview ในเกมทุกครั้ง

## ที่มา

- [THE ULTIMATE 100% TRAIT FUSION GUIDE! PERFECT 5/5 — GTJanne](https://www.youtube.com/watch?v=lyNM0s2CUIY)
- [Deviations and Fusion: An Overview — 足長よしお (note.com)](https://note.com/elias04201/n/n07ff10ec45cc?hl=en)
- [Once Human Deviant Traits — Gaming with Daopa](https://gamingwithdaopa.ellatha.com/once-human/deviant-traits/)
- [Fusion Tracker](https://fusiontracker.io/)

โปรเจกต์แฟนเมด ไม่เกี่ยวข้องกับ Starry Studio
