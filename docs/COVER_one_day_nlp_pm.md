# 표지 지시문 — 「하루에 다 끝내는 자연어 분석 서머리 노트 · 저녁반」

> 최신 프롬프트와 전체 그림 목록은 `docs/IMG_one_day_nlp_pm.md`(대화 1~3)를 따릅니다. 아래는 첫 판 기록입니다.

## 지금 상태

- `cover_one_day_nlp_pm.webp` (1920×1080, 무손실): 캐릭터 팩의 96px 픽셀 그림(시아 E17 하품, 모아 E01 찻잔)을 2배로 키워, 640×360 격자에 그린 저녁 연구실 배경 위에 얹었습니다. 전체를 `NEAREST` 3배로 키워 픽셀 경계가 또렷합니다.
- 머신러닝 편(오전반, 하품하는 시아)·딥러닝 편(오후반, 모아)과 짝을 맞춰 **저녁반 = 해 질 녘, 시아 하품 + 모아 찻잔**으로 정했습니다.
- 더 다듬은 그림을 받으면 아래 프롬프트로 만든 그림으로 바꿉니다. `index.html`은 그대로 두고 파일만 교체합니다(원격자 480×270 또는 640×360을 정수배로).

## Genspark 요청 (16비트 RPG 픽셀아트)

**참고 이미지 (함께 올리기):** 캐릭터 팩 `images/sia/E17_sleepy.png`, `images/moa/E01_*.png`, 오전반 표지

```
16-bit RPG pixel art, wide 16:9 scene on a native 480x270 pixel grid, crisp pixels, limited palette, no anti-aliasing.
A small research lab office at dusk: a wide window with purple-to-orange sunset sky and a pixel city skyline with lit windows.
Two characters behind a long wooden desk, drawn in the same pixel style as the attached character sheets:
left, a calm young woman with long straight jet-black hair and a gray bow, maid dress with white apron, covering a big yawn with her hand, eyes half closed;
right, a gentle young woman with long ash-beige wavy hair and a white frilled headband with a ribbon over her left ear, camel cardigan, smiling with eyes closed, holding a pink tea cup with both hands.
On the desk: a laptop, an open notebook, a small monitor showing colorful bar charts.
Floating above them: two speech bubbles containing small colored blocks, and a row of small colored square tiles turning into bars (text becoming tokens and numbers).
Bright and warm overall, white-ish wall so it sits well on a white web page.
No readable text, no letters, no numbers, no logos.
```

## 점검

- 픽셀 격자가 고른가(4배 확대해도 경계가 또렷한가)
- 시아: 흑발 생머리, 하품 / 모아: 애쉬 베이지 웨이브, 왼쪽 귀 위 리본, 찻잔 (좌우 반전 금지)
- 그림 안에 읽히는 글자가 없는가
- 바탕이 밝은가 (페이지가 흰 바탕)
