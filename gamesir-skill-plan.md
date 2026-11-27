# แผนการใช้สกิล: คลิป GameSir (จอยสีขาว ปุ่มอนาล็อกขอบแดง)

## คลิปที่ได้รับ
| ไฟล์ | ครีเอเตอร์ (จากชื่อไฟล์/ลายน้ำ) | ยาว | เนื้อหา | ข้อความ/ลายน้ำในคลิป |
|---|---|---|---|---|
| 1 | stvnsavvy | 28.0 s | แกะกล่อง (กล่องเขียน NOVA 2 …), จับปุ่ม, ตัวรับสัญญาณ, เล่นเกมบนทีวี | มีตัวหนังสือฝัง: "Membrane ABXY buttons", "GameSir Hall Effect sticks", "Designed for Switch, PC, Android and iOS" ฯลฯ |
| 2 | keno.finds | 22.6 s | ถือจอยโคลสอัพ กดปุ่ม/อนาล็อก/ทริกเกอร์ ห้องโทนขาว | ไม่เห็นข้อความฝัง |
| 3 | jamesreviewtv | 43.3 s | แกะกล่อง (ANTI stick-drift), สาย, ดองเกิล, ใช้กับโน้ตบุ๊ก/เครื่องพกพา | มีข้อความฝัง: "TRI-MODE CONNECTIVITY", "1000HZ POLLING RATE", "DUAL ASYMMETRIC MOTORS", "FULL CUSTOMIZATION" + ลายน้ำ @jamesreviewtv |

ข้อสังเกต: ทั้ง 3 คลิปเป็นของครีเอเตอร์คนอื่น; รุ่นดูเหมือนกัน (GameSir สีขาว ขอบอนาล็อกแดง กล่องเขียน NOVA 2 …) แต่ต้องยืนยันชื่อรุ่นเต็มจากกล่องและเว็บแบรนด์ก่อน ถ้ามีคลิปไหนเป็นรุ่นอื่นต้องแจ้งเจ้าของ

## สกิลที่มีทั้งหมด (คัดตามความเกี่ยวข้อง)
- ห้ามใช้ (กฎเจ้าของ): thai-tiktok-ad-editor-reach, tiktok-product-video-editor, pun-hook-beat-montage, maincontent-beat-montage
- ไม่เกี่ยวกับงานนี้: กลุ่ม affiliate/blog/SEO/email/landing page/YouTube long-form/ig-carousel/ig-dm ฯลฯ, apple-launch-film, title-sequence-3d, animated-chart, milestone-reveal, model-showdown, vox-explainer, loop-cover

## แผน: ขั้นตอน × สกิล
| ขั้น (ตาม CLAUDE.md) | สกิลที่เรียกจริง (Skill tool) | ใช้ทำอะไร | ผลลัพธ์ |
|---|---|---|---|
| 1 วางแผน | (แผนนี้) + ผู้ตรวจสกิลอิสระ | ตรวจว่าเลือกสกิลถูก/ครบ | แผนที่ผ่านการตรวจ |
| 2 เช็คคลิป | – (ffmpeg scene detection + ดูเฟรม) | รุ่นเดียวกันไหม, จุดตัดต้นฉบับ, ตำแหน่งข้อความฝัง/ลายน้ำ | ตารางช่วงที่ใช้ได้ |
| 3 สเปก | content-research-brief (ตั้ง product.url = gamesir.com, เอาตัวเลขจากเว็บแบรนด์เท่านั้น ไม่เอาจากบล็อก) | ค้นสเปกจริงจาก gamesir.com พร้อมลิงก์ | ตารางสเปก + แหล่งที่มา |
| 3b ประเมินสินค้า | purple-cow-audit | จุดเด่นจริงที่ควรขาย | คะแนน + มุมขาย |
| 3c เลือกมุม | content-angle-ranker | จัดอันดับมุมคอนเทนต์ (เช่น Hall Effect ไม่ดริฟต์, ใช้ได้หลายเครื่อง) | มุมหลัก 1 มุม |
| 4 ฮุก | ig-reel (hookscore.py) | ฮุก 5 ข้อคะแนนสูง น่าเชื่อ | ให้เจ้าของเลือก |
| 4b สคริปต์พากย์ | tiktok-script-writer (ตัดท่อน CTA, #ad, disclosure, ฮุกที่มีราคา ออก) → mindfluence → ig-human; ig-reel beats.py จับท่อนพากย์ 3 ท่อนให้ตรงช่วงภาพ | สคริปต์ 3 ท่อน ภาษาพูดจริง + คำสั่งสไตล์เสียง | สคริปต์ส่งให้ AI อ่าน |
| 4c ตรวจคำต้องห้าม | – (เช็กลิสต์จาก CLAUDE.md เอง; ไม่ใช้ compliance-checker เพราะสกิลนั้นสั่งให้เพิ่ม disclosure/disclaimer ซึ่งเจ้าของห้าม) | ไม่มีราคา/CTA/disclaimer/สเปกเกินจริง | ผ่าน/แก้ |
| 5 วางแผน motion graphic | motionmaxxing (judgment/slop/director/transitions) + video-shotcraft (references/shots) | ตาราง ช่วงเวลา × จุดขาย × กราฟิกเกาะตัวสินค้า × การ์ด × ตำแหน่ง; หลีกเลี่ยงหน้าตา AI ทั่วไป | แผนให้เจ้าของดู |
| 6 ตัดต่อ | video-shotcraft (การ์ด + demo TSX, Remotion) + motionmaxxing look.py (lint.mjs รันกับ Remotion ไม่ได้ เพราะรับแค่ไฟล์ HTML: ตรวจ G5 แทนด้วยตาจาก look/sheet.jpg และแจ้งเจ้าของ); ไม่ใช้ motion-effects เพราะเป็นลูป HTML 8 วิที่มีช่วงค้าง ไม่ใช่งานบนฟุตเทจ | ตัดต่อจริง | draft |
| 6b เสียง | video-shotcraft (คลัง SFX + README คู่ภาพ/เสียง) + motionmaxxing sound-sync.md, sync.mjs, mix.py | วางเสียงพากย์/เอฟเฟกต์, -14 LUFS | mix |
| 7 ผู้ตรวจอิสระ | subagent context สะอาด + final-review.md + aesthetic-rules.md | ตรวจก่อนส่ง แก้จนผ่านและไม่มีข้อค้าง | PASS |
| 8 ตรวจไฟล์ส่ง | reel-export (สเปกไฟล์ TikTok 1080x1920, H.264, yuv420p, bt709, safe zone, ffprobe) + motionmaxxing look.py + ffmpeg ebur128 (-14 LUFS) | ภาพ เสียง ความดัง | ส่งไฟล์ |

## เงื่อนไขภาพที่ต้องระวังกับคลิปชุดนี้
- คลิป 1 และ 3 มีตัวหนังสือฝัง + ลายน้ำ: ห้ามวางข้อความทับ, ห้ามซูมเพื่อซ่อน; เลือกช่วงที่ไม่มีข้อความ หรือแจ้งเจ้าของถ้าเลี่ยงไม่ได้
- ใช้ครบทั้ง 3 คลิป, เห็นสินค้าเต็มตัว, ไม่เพิ่มความสว่างเอง (ตามที่เจ้าของสั่งรอบ G213), ไม่ใส่เพลงถ้าไม่สั่ง
- video-shotcraft: ข้ามส่วน "交付收尾" (เปิด workbench, ชวนแท็ก/ส่งโชว์เคส) และไม่โหลด SFX จาก Freesound ใช้คลังในเครื่องเท่านั้น

## แก้ตามผู้ตรวจสกิล (รอบ 1)
- ตัด compliance-checker, motion-effects; เพิ่ม reel-export, ig-reel beats.py; กำกับ content-research-brief และ tiktok-script-writer
