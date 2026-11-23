# 이미지 제작 명세서 — 「하루에 다 끝내는 자연어 분석 서머리 노트 · 저녁반」

> 그림체: **16비트 RPG 픽셀아트** (연구실 시리즈 지침). 페이지 바탕이 흰색이므로 그림도 밝게.
> 생성 도구: Genspark. 대화 하나에 같은 비율 그림 3~5장씩. **대화 1의 표지를 먼저 받아 그림체를 확정**한 뒤, 그 표지를 이후 대화에 참고 그림으로 함께 올립니다.

## 0. 다시 검토한 결과 (2026-11-23)

| 자리 | 지금 | 문제 | 할 일 |
|---|---|---|---|
| 표지 `cover_one_day_nlp_pm.webp` | 캐릭터 팩 96px 그림을 손으로 그린 배경에 얹은 임시판 | ① 아래 4분의 1이 빈 책상 다리뿐 ② 캐릭터가 상반신 스티커처럼 떠 보임 ③ 배경과 캐릭터의 픽셀 크기가 다름(캐릭터 2배, 배경 3배) | 대화 1-①로 교체 |
| 공유 미리보기 `og_…jpg` · 썸네일 `thumb_…webp` | 임시 표지에서 자름 | 표지와 같은 문제 | 새 표지에서 다시 자름 |
| 교시 머리 6곳 (`data-img="sc_period1~6"`) | 움직이는 작은 도표만 있음 | 그림 자리 비어 있음(선택) | 대화 3 |
| 부록 실전 연습장 | 그림 없음 | 첫 화면이 글뿐 | 대화 2-① |
| 종례 모의 면접 | 그림 없음 | 선택 | 대화 2-② |

## 1. 캐릭터 고정 묘사 (모든 프롬프트 공통)

| 이름 | 외형 (영어 프롬프트에 그대로) |
|---|---|
| 시아 | long straight jet-black hair with side-swept bangs, gray eyes, small drop earrings, charcoal-black maid dress with a large gray bow and white frilled apron |
| 모아 | long ash-beige wavy hair, white frilled maid headband with a ribbon over her LEFT ear, amber eyes, camel knit cardigan over a white blouse and white frilled apron |
| 박사 | messy black hair with a white streak, round glasses, white lab coat over a dark vest and tie |
| 조수 하루 | long pink hair with navy streaks tied in two side buns, blue eyes, oversized lavender hoodie |
| 초파리 연구원 | humanoid fruit fly with big red compound eyes, translucent wings, a small white lab coat, colorful cables on the head |
| 주판봇 | boxy beige retro-computer robot, green screen face with a simple smile, antenna, holding a wooden abacus |

참고 그림(함께 올리기): `adminmrobo/fruitfly-lab-expressions`의 각 캐릭터 기본 그림 + 시아 `E17`(하품), 모아 `E01`(찻잔).

## 2. 저장 이름 체크리스트

| 순서 | 파일 | 비율·원격자 | 반영 크기 |
|---|---|---|---|
| 1-① | `cover_one_day_nlp_pm.webp` | 16:9 · 480×270 | 4배 1920×1080 무손실 WebP |
| 1-② | `og_one_day_nlp_pm.jpg` | 1-①에서 400×210 자름 | 3배 1200×630 |
| 1-③ | `thumb_one_day_nlp_pm.webp` | 1-①에서 300×200 자름 | 2배 600×400 |
| 2-① | `practice/cover_practice.webp` | 16:9 · 480×270 | 4배 1920×1080 |
| 2-② | `sc_final_interview.webp` | 16:9 · 480×270 | 4배 |
| 3-①~⑥ | `sc_period1.webp` ~ `sc_period6.webp` | 3:2 · 300×200 | 4배 1200×800 |

반영 규칙: 생성 PNG를 4로 나눈 원래 격자를 찾아 `NEAREST` 정수배로만 키움. 손실 압축·정수배 아닌 축소 금지. 페이지에는 `image-rendering:pixelated`가 이미 들어 있음.

---

## 대화 1 — 표지 (16:9, 먼저)

```
16-bit RPG pixel art, wide 16:9 illustration on a native 480x270 pixel grid, crisp hard-edged pixels, limited palette, no anti-aliasing, no dithering noise.
Scene: a small cozy research lab at dusk. A wide window across the back wall shows a purple-to-orange sunset sky and a pixel city skyline with warm lit windows. Interior wall is bright cream so the image sits well on a white web page.
Two characters sit side by side behind a long wooden desk, shown from the waist up, full upper body visible, same pixel scale as the background:
LEFT: a calm young woman with long straight jet-black hair and side-swept bangs, gray eyes, small drop earrings, charcoal-black maid dress with a large gray bow and white frilled apron. She covers a big yawn with her right hand, eyes half closed and slightly teary.
RIGHT: a gentle young woman with long ash-beige wavy hair, a white frilled maid headband with a ribbon over her LEFT ear, amber eyes, camel knit cardigan over a white blouse and white frilled apron. She smiles with eyes closed, holding a pink tea cup with both hands.
On the desk: an open notebook with blank lines, a laptop, a small monitor showing colorful bar charts, a desk lamp.
Floating in the air above them, symbolising "words become numbers": two speech bubbles filled with small colored rectangles (no letters), and a stream of small colored square tiles that turn into a little bar chart.
Composition: characters in the central area with 12% margin left and right; keep the upper-left area calm and bright; the desk edge sits at about 80% of the height so the lower area is not empty.
Mood: sleepy but warm, the last study session of a long day.
No readable text, no letters, no numbers, no logos, no real brands.
```

**고칠 때 (같은 대화에서):** `Same characters, same pixel grid and composition. Change only: {고칠 점}. Still no text.`

점검: 왼쪽 시아 하품·흑발, 오른쪽 모아 찻잔·리본은 왼쪽 귀 위(좌우 반전 금지), 글자 없음, 픽셀 크기가 캐릭터와 배경에서 같은가.

---

## 대화 2 — 부록과 종례 (16:9, 대화 1의 표지를 참고 그림으로 함께 올림)

**2-① 실전 연습장 표지**
```
Same pixel art style, palette and pixel scale as the attached cover. 16:9, native 480x270 grid, crisp pixels, no anti-aliasing.
Scene: a cheerful small online-shop back office called by its look only (no sign text): shelves of parcels and boxes, a big wall monitor with three panels — a review board with green and pink thumbs, a customer-inbox with grouped colored envelopes, and a chat window with speech bubbles.
The black-haired maid girl (gray bow) sits at a desk sorting envelopes into colored trays; the ash-beige haired girl with the ribbon over her LEFT ear stands beside her pointing at the wall monitor with a bright smile.
In the corner, a boxy beige retro-computer robot with a green smiling screen face holds a wooden abacus; a small humanoid fruit fly in a white lab coat with big red eyes peeks from behind a parcel with a clipboard.
Bright daytime light, white-ish walls.
No readable text, no letters, no numbers, no logos.
```

**2-② 종례 · 모의 면접**
```
Same pixel art style, palette and pixel scale as the attached cover. 16:9, native 480x270 grid, crisp pixels.
Scene: a small interview room at night with one window showing a dark blue sky and stars. A professor with messy black hair with a white streak, round glasses and a white lab coat sits behind a table holding a stack of blank cards, smiling kindly.
Across the table, the black-haired maid girl (gray bow) sits upright and nervous but determined; next to her the ash-beige haired girl (ribbon over her LEFT ear) gives a small thumbs-up.
On the table: flash cards, two cups of tea, a small hourglass.
Warm lamp light, calm and encouraging mood.
No readable text, no letters, no numbers, no logos.
```

---

## 대화 3 — 교시 머리 그림 6장 (3:2, 3장씩 두 대화로 나눠도 됨)

공통 머리말 (각 요청 앞에 붙이기):
```
Same pixel art style, palette and characters as the attached cover. 3:2 ratio, native 300x200 pixel grid, crisp hard-edged pixels, no anti-aliasing, bright white-ish background. No readable text, no letters, no numbers, no logos.
```

**3-① 1교시 · 사람 말을 읽는 컴퓨터** — `The ash-beige haired girl (ribbon over LEFT ear) holds up a speech bubble; colored rectangles flow out of it into a small computer screen that shows a tidy table. The professor in a lab coat watches with a hand on his chin.`

**3-② 2교시 · 글 다듬고 자르기** — `The black-haired maid girl uses small pixel scissors to cut a long paper strip of colored blocks into small square tiles; a few gray dust-like scraps fall into a trash bin, but one pink tile marked only by its color is being rescued by a small humanoid fruit fly in a lab coat.`

**3-③ 3교시 · 글자를 숫자로** — `A boxy beige retro-computer robot with a green screen face counts colored tiles on a wooden abacus; beside it a pink-haired girl with two side buns and a lavender hoodie holds a map where colored dots form small clusters.`

**3-④ 4교시 · 글에 딱지 붙이기** — `The ash-beige haired girl highlights blocks on a long paper strip with highlighter pens in yellow, green, blue and orange; the black-haired girl sorts small cards into two trays, one with a blue smile icon and one with a pink frown icon.`

**3-⑤ 5교시 · 트랜스포머와 LLM** — `A row of small square tiles on a table, each connected to every other tile by glowing orange arcs of different thickness, like a group chat; the professor points at the arcs while the pink-haired girl with side buns looks amazed.`

**3-⑥ 6교시 · 찾고, 재고, 쓰기** — `A magnifying glass over a stack of envelopes grouped by color; next to it a small fishing net holding some fish over a pond, with a few fish still in the pond; the fruit fly researcher in a lab coat checks a clipboard with green check marks.`

점검: 6장 모두 같은 픽셀 크기·팔레트인가, 캐릭터 외형이 1장의 고정 묘사와 같은가, 글자가 없는가.

---

## 반영 순서

1. 대화 1 → 표지 교체, og·썸네일 다시 자르기 (alt 문구는 그대로 맞음).
2. 대화 2 → 연습장 머리와 종례 머리에 `<img>` 추가.
3. 대화 3 → 교시 머리 `figure.stage2`의 글 상자 옆에 그림 추가(움직이는 도표는 유지).
