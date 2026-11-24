# Midas Chart

กราฟเทรดแบบ single-file (HTML + lightweight-charts) · ธีม Chrome Hearts All Black

## ฟีเจอร์
- Timeframe: 1m / 5m / 15m / 1h / 4h / 1d / 1w / 1M (Binance spot/futures + หุ้น US ผ่าน Yahoo)
- แถบอ่าน stage แบบ Wyckoff — 🟢 ควรซื้อ · 🔴 ไม่ควรซื้อ · 🟡 Wait & See
- Long/Short position ปรับขนาดได้จากมุมและขอบทั้ง 4 ด้าน
- Thumbnail ของสินทรัพย์ใน watchlist
- ธีม: Chrome Hearts, Zeus, Midas, Dark, Light
- รองรับมือถือ/แท็บเล็ต: Watchlist เป็นลิ้นชักปุ่ม ☰ · แตะ/ลากนิ้ววาดและยืดหด Long/Short · กดค้างที่รายการ Watchlist เพื่อลบ · เพิ่มลงหน้าจอโฮมเป็นแอปได้ (PWA)

> Wyckoff stage เป็นสูตร heuristic เพื่อช่วยประกอบการตัดสินใจ ไม่ใช่คำแนะนำการลงทุน

## Deploy บน Netlify
1. Push โฟลเดอร์นี้ขึ้น GitHub
2. Netlify → **Add new site → Import an existing project** → เลือก repo
3. Build command: เว้นว่าง · Publish directory: `.` (ค่าใน `netlify.toml` ตั้งไว้แล้ว)
4. กด Deploy

หรือลากทั้งโฟลเดอร์ไปวางที่ https://app.netlify.com/drop

## ใช้บนมือถือ / แท็บเล็ต
เปิดลิงก์ Netlify แล้วเลือก **Add to Home Screen** (iOS: Share → Add to Home Screen · Android: เมนู ⋮ → Install app) จะเปิดเต็มจอเหมือนแอป

## รันในเครื่อง
เปิด `index.html` ในเบราว์เซอร์ได้เลย (ต้องออนไลน์เพื่อโหลดไลบรารีกราฟ ข้อมูลราคา และไอคอน)

## หมายเหตุ
- ข้อมูลที่ผู้ใช้ตั้งค่า (watchlist, เส้นที่วาด, ธีม) เก็บใน localStorage ของเบราว์เซอร์
- หุ้น US ดึงผ่าน CORS proxy สาธารณะ อาจช้า/ล่มเป็นบางช่วง
- โลโก้และลวดลาย Chrome Hearts เป็นเครื่องหมายการค้าของเจ้าของ ใช้เพื่อตกแต่งส่วนตัว หากเปิดเว็บสาธารณะเชิงพาณิชย์ควรเปลี่ยนเป็นงานออกแบบของตนเอง
