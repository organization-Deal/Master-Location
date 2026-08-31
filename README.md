# Deal Location Workspace

เว็บ Workspace สำหรับทีม Location Acquisition โดยแยกงาน Prospecting ออกจาก Master Location / Contract workflow

## วิธีเปิด
- เปิด `index.html` ได้ทันทีบน Browser
- หรืออัปโฟลเดอร์ทั้งหมดขึ้น Cloudflare Pages / GitHub Pages ได้เลย (Static Site, ไม่ต้อง build)

## ฟีเจอร์หลัก
- Monthly KPI: 300 ร้านใหม่ / 20 ร้านที่ปิดได้ (แก้ Target ได้)
- Target Location CRM + Search / Filter / Score / Owner / Follow-up
- Duplicate checker เทียบกับ Installed Locations ที่ seed จากรายชื่อที่ให้มา
- Pipeline แบบ Kanban
- On Tour Intelligence: Paste `วง | ร้าน | จังหวัด | วันที่ | URL` แล้วแตกเป็น Candidate Location
- Research Inbox เช็กร้านเก่าก่อนสร้าง Lead
- Team Performance
- Contact Brief สำหรับเตรียมทีมก่อนโทร/ทัก
- Export Target CSV
- Export Won locations เป็น CSV สำหรับส่งต่อ Master Location เดิม
- JSON Backup / Restore
- เก็บข้อมูลใน localStorage ของ Browser (เวอร์ชันนี้ยังไม่ใช่ multi-user database)

## แนวทาง production ต่อ
1. เปลี่ยน localStorage เป็น Cloudflare D1
2. เพิ่ม Login + Team roles
3. Activity log ต่อ user
4. Integrate Google Maps / Places หรือข้อมูลภายนอกที่ได้รับอนุญาต
5. Import Excel Master Location ผ่าน backend
6. Notification LINE OA เมื่อ Follow-up ถึงกำหนด
