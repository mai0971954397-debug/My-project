# SFX library (original, synthesized — free to use)

Six short UI/edit sound effects, 44.1 kHz mono WAV, peak -1 dBFS. Synthesized from scratch
(numpy), modelled on the common "viral edit" sound categories. No third-party audio inside.

| file | ชื่อเสียง | length | hit point | ใช้ตอนไหน (when to use) |
|---|---|---|---|---|
| `charge-data-ui.wav` | Charge + Data UI | 1.3 s | ~0.72 s (riser peak, blips follow) | ก่อนเปิดตัวสินค้า / ตัวเลขหรือสเปกเด้งขึ้น: วางให้จุด 0.72 s ตรงเฟรมที่ข้อความหรือ UI โผล่ |
| `charge-clicks.wav` | Charge + Clicks | 1.2 s | ~0.62 s (first click) | ชาร์จพลังแล้วตัดภาพเร็ว 3–4 ช็อต: แต่ละคลิกตรงกับแต่ละคัต |
| `camera-flash.wav` | Camera Flash | 0.9 s | 0.0 s | แฟลชขาว / เฟรมค้างแบบถ่ายรูป / จังหวะ "ถ่ายรูปสินค้า" |
| `popup-flash.wav` | Pop Ups + Camera Flash | 1.4 s | pops 0 / 0.13 / 0.24 s, flash 0.42 s | สติกเกอร์หรือป้ายเด้ง 3 อันแล้วจบด้วยแฟลช |
| `data-clicks-ui.wav` | Data Clicks + UIs | 1.0 s | starts 0.0 s | ข้อความพิมพ์ขึ้น, ไอคอน/ข้อมูลไหลขึ้นจอ, รายการสเปกเลื่อน |
| `mechanical-clicks.wav` | Mechanical Clicks | 1.3 s | starts 0.0 s | ตัวหนังสือขึ้นทีละคำ, คีย์บอร์ด, ปุ่มกด, CTA ปิดท้าย |

## How to use
- Line up the **hit point** with the picture event (cut, text landing, flash frame), not the file start.
- Gain: hits around -6 to -3 dB, background ticks -14 to -10 dB. Leave silence right before the main hit.
- Use 1–3 hero sounds per 20 s clip; do not stack a sound on every cut.
- motionmaxxing: add to `events.json` → `{"t": <hit time - hit point>, "sfx": "<path>/charge-data-ui.wav", "gain": -6}` then `mix.py --events`.
- Remotion (video-shotcraft template): copy into `public/audio/` and use `<Audio src={staticFile('audio/camera-flash.wav')} />` inside a `<Sequence from={frame}>`.

## คู่ เอฟเฟกต์ภาพ + เสียง (จากคลิปตัวอย่างที่เจ้าของส่งมา "With This / Use This")
หลัก: เสียงต้องเป็นชนิดเดียวกับการเคลื่อนไหวของภาพ และจุดดังที่สุดของเสียงตรงกับเฟรมที่เอฟเฟกต์แรงที่สุดพอดี (ในคลิปตัวอย่าง เสียงลงเฟรมเดียวกับภาพทุกครั้ง)

| เอฟเฟกต์ภาพ (ชื่อใน CapCut) | ลักษณะภาพ | เสียงที่คู่กัน (ชื่อใน CapCut) | ในคลังนี้ใช้แทนได้ |
|---|---|---|---|
| Slide Left | ภาพสไลด์ข้างพร้อมเส้นเบลอแนวนอน | Deep woosh | `whoosh` (ลงเสียงต่ำ หางยาว) |
| Glare | แสงขาวจ้าวาบบนตัวแบบ | Camera shutter "Kasha" | `camera-flash.wav` |
| Brush Glitch | ภาพแตกเป็นแถบ glitch | Glitch sound logo match | ยังไม่มีในคลัง |
| Shake & Flash | ภาพสั่นพร้อมแฟลชขาว | Camera flash sound | `camera-flash.wav` + impact |

## ชุดเสียงฮุก/ไรเซอร์ (จากคลิปตัวอย่างที่เจ้าของส่งมา: "Hook 1/2/3, Tension Riser")
ยังไม่มีไฟล์ในคลัง (คลิปเป็นตัวอย่างพรีวิว 360p) ใช้เป็นแนวทางเลือกเสียง:

| เสียง | ลักษณะที่วัดได้ | ใช้ตอนไหน |
|---|---|---|
| Hook 1 (~3 วิ) | เสียงลมแหลมแบบ glitch ค่อย ๆ เพิ่มเบส แล้วตูมเบสต่ำที่ ~2.7 วิ แล้วตัดเงียบทันที | ใต้ฮุก 0–3 วิแรก: ให้จุดตูมตรงเฟรมที่ข้อความฮุกลงตัว/ตัดเข้าสินค้า |
| Hook 2 (~6 วิ) | เบสต่ำตีเป็นจังหวะต่อเนื่อง สลับช่วงลมโปร่ง | เป็นจังหวะคล้ายเพลง: ใช้เฉพาะเมื่อเจ้าของสั่งให้มีเพลง/บีท |
| Tension Riser (~4 วิ) | เสียงทุ้มไต่ระดับสูงขึ้นและดังขึ้นเรื่อย ๆ แล้วหยุดตัดฉับ | นำเข้าจุดเปิดตัวสินค้า/ตัวเลขสเปก: ให้จุดหยุดตรงเฟรมคัตพอดี |
| Hook 3 (~4 วิ) | เสียงกลางสั้น ๆ แล้วเงียบ ~0.4 วิ ก่อนเบสกระแทก | จุดเฉลย: เว้นเงียบก่อนช็อตสินค้า/ชื่อรุ่น แล้วกระแทกพร้อมภาพ |

ระดับเสียงใต้เสียงพากย์: ลดลงให้เสียงพากย์ดังกว่าเสมอ (ดู motionmaxxing `references/sound-sync.md` ข้อ 8)
