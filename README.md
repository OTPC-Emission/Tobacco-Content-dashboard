# Tobacco Product Composition Public Site

เว็บสำหรับเผยแพร่ข้อมูลราย Product จาก `latest.xlsx`

## โครงสร้างที่ตรวจพบในไฟล์ล่าสุด
- Product: 19
- มี Tar/Nicotine/CO ครบ: 18
- สูงกว่าค่าที่กำหนดอย่างน้อย 1 สาร: 8
- Product ที่พบชื่อส่วนประกอบตรงกับบัญชีอ้างอิง: 16
- รายการส่วนประกอบดิบ: 1131
- ชื่อส่วนประกอบหลัง normalize: 310

## Logic
- Tar > 10 mg/มวน = สูงกว่าค่าที่กำหนด
- Nicotine > 1 mg/มวน = สูงกว่าค่าที่กำหนด
- CO > 10 mg/มวน = สูงกว่าค่าที่กำหนด
- 80–100% ของค่าที่กำหนดใช้สีส้มเพื่อสื่อว่าเข้าใกล้ค่าที่กำหนด
- จับคู่ชื่อสารแบบ Strict Match เท่านั้น
- Alias ที่อนุญาต เช่น Glycerin/Glycerine = Glycerol, L-Menthol = Menthol, L-Menthone = Menthone
- ไม่รวม Ethyl Maltol เป็น Maltol, Ethyl Vanillin เป็น Vanillin หรือ 4-Methoxybenzaldehyde เป็น Benzaldehyde

## GitHub Pages
อัปไฟล์ต่อไปนี้ไว้ใน repository:
- index.html
- .nojekyll
- data/latest.xlsx

เมื่อแทนที่ `data/latest.xlsx` โดยยังคงโครงสร้างคอลัมน์เดิม เว็บไซต์จะอ่าน Product และคำนวณใหม่ตอนเปิดหน้าเว็บ
