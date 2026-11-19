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
