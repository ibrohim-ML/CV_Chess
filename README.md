<p align="center">
  <strong>♚ CV Chess ♔</strong><br>
  <em>Touchless. Intuitive. Chess.</em>
</p>

<p align="center">
  Control the chessboard with nothing but your hand — <br>
  no mouse, no keyboard, no touchscreen. Just you and the camera.
</p>

<br>

---

# CV Chess

> **Camera-controlled chess game using real-time hand tracking**

CV Chess is a browser-based chess game that uses **MediaPipe Hands** to track your fingers in real time. Point at pieces, pinch to grab, release to move — all without touching a thing.

---

## ✨ Features

- **Hand tracking** — index finger controls the cursor; pinch with thumb to grab
- **Full chess rules** — enforces legal moves, check, checkmate, and pawn promotion
- **Real-time feedback** — on-screen cursor, debug panel, and status indicators
- **Smooth cursor** — adaptive smoothing for natural hand movement
- **Responsive** — works on desktop and tablet browsers
- **No dependencies** — pure HTML, CSS, and JavaScript

---

## 🎮 How It Works

| Action | Gesture |
|--------|---------|
| Move cursor | Move your index finger |
| Grab a piece | Pinch (bring thumb and index together) |
| Release / move | Open your hand |

The camera feed is processed entirely in the browser via **MediaPipe**. Your hand landmarks are mapped to board coordinates, and a hysteresis-based pinch detector ensures stable grab/release transitions.

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| Hand tracking | [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) |
| Rendering | HTML5 Canvas + CSS Grid |
| Camera | MediaPipe Camera Utils |
| Logic | Vanilla JavaScript (ES6) |

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/ibrohim-ML/CV_Chess.git
cd CV_Chess

# Start a local server
python -m http.server 8000
```

Open **http://localhost:8000** in your browser and click **"Kamerani yoqish"** to begin.

> **Note:** Camera access requires **localhost** or **HTTPS**. Use the local server above — do not open the file directly (`file://`).

---

## 📁 Project Structure

```
CV_Chess/
├── index.html      # All game logic, styles, and markup
├── README.md       # This file
└── .gitignore
```

Everything is in a single HTML file — no build tools, no bundlers, no frameworks.

---

## 🧠 Architecture

The game runs a fixed-timestep animation loop (`requestAnimationFrame`) that:

1. Reads the latest hand landmarks from MediaPipe
2. Maps normalized coordinates to board-local pixel space
3. Applies adaptive smoothing for jitter reduction
4. Detects pinch state with hysteresis (ON at < 0.035, OFF at > 0.050)
5. Computes legal moves using a full chess engine (pseudo-legal → king-safe filter)
6. Renders the board, cursor, drag ghost, and UI overlays

The chess engine includes:

- All piece movement logic (pawn, knight, bishop, rook, queen, king)
- Sliding-piece ray casting with early termination
- Check detection via attacker square scanning
- Legal move filtering (cannot move into check)
- Checkmate and stalemate detection
- Automatic pawn promotion to queen

---

## 🖼️ Screenshots

<details>
<summary>Click to expand</summary>

— *Screenshots coming soon* —

</details>

---

## 🧪 Browser Support

| Browser | Status |
|---------|--------|
| Chrome | ✅ Fully supported |
| Firefox | ✅ Supported |
| Safari | ⚠️ May require localhost |
| Edge | ✅ Supported |

<br>

<h1 align="center">♚ CV Chess ♔</h1>
<p align="center"><em>Sensorlarsiz. Intuitiv. Shaxmat.</em></p>
<p align="center">Shaxmat taxtasini faqat qo'lingiz bilan boshqaring —<br>sichqoncha, klaviatura yoki sensor kerak emas. Faqat siz va kamera.</p>

---

## CV Chess

> **Real vaqt rejimida qo'l tracking orqali boshqariladigan veb-shaxmat**

CV Chess — bu **MediaPipe Hands** yordamida barmoqlaringizni real vaqtda kuzatib, shaxmat o'ynash imkonini beruvchi brauzer ilovasi. Barmoq bilan ko'rsatasiz, chimchib ushlaysiz, qo'yib yuborib yurish qilasiz — hech narsaga tegmasdan.

---

## ✨ Xususiyatlar

- **Qo'l tracking** — ko'rsatkich barmoq kursor vazifasini bajaradi; chimchish bilan ushlash
- **To'liq shaxmat qoidalari** — qonuniy yurishlar, shox, shox-mat va piyodani almashtirish
- **Real vaqt rejimi** — ekrandagi kursor, debug paneli va holat ko'rsatkichlari
- **Silliq kursor** — moslashuvchan tekislash tabiiy harakat uchun
- **Responsiv** — desktop va planshet brauzerlarida ishlaydi
- **Hech qanday kutubxona kerak emas** — sof HTML, CSS va JavaScript

---

## 🎮 Qanday ishlaydi

| Harakat | Imo-ishora |
|---------|------------|
| Kursorni harakatlantirish | Ko'rsatkich barmoqni siljitish |
| Piyodani ushlash | Chimchish (bosh va ko'rsatkich barmoqni birlashtirish) |
| Qo'yib yuborish / yurish | Qo'lni ochish |

Kamera tasviri to'liq brauzer ichida **MediaPipe** orqali qayta ishlanadi. Qo'l nuqtalari taxta koordinatalariga moslashtiriladi va maxsus detektor barqaror ushlash/qo'yib yuborishni ta'minlaydi.

---

## 🧰 Texnologiyalar

| Qatlam | Texnologiya |
|--------|-------------|
| Qo'l tracking | [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) |
| Chizish | HTML5 Canvas + CSS Grid |
| Kamera | MediaPipe Camera Utils |
| Logika | Sof JavaScript (ES6) |

---

## 🚀 Ishga tushirish

```bash
# Reponi klonlash
git clone https://github.com/ibrohim-ML/CV_Chess.git
cd CV_Chess

# Mahalliy serverni ishga tushirish
python -m http.server 8000
```

Brauzerda **http://localhost:8000** ni oching va **"Kamerani yoqish"** tugmasini bosing.

> **Eslatma:** Kamera ishlashi uchun **localhost** yoki **HTTPS** kerak. Faylni to'g'ridan-to'g'ri (`file://`) ochmang.

---

## 📁 Loyiha tuzilishi

```
CV_Chess/
├── index.html      # Barcha o'yin logikasi, stillar va markup
├── README.md       # Ushbu fayl
└── .gitignore
```

Hammasi bitta HTML fayl ichida — hech qanday build tool, bundler yoki framework kerak emas.

---

## 🧠 Arxitektura

O'yin `requestAnimationFrame` orqali doimiy siklda ishlaydi:

1. MediaPipe dan oxirgi qo'l nuqtalarini oladi
2. Normalizatsiyalangan koordinatalarni taxta piksellariga moslashtiradi
3. Jitter kamaytirish uchun moslashuvchan tekislash qo'llaydi
4. Gisterezis asosida chimchish holatini aniqlaydi (ON < 0.035, OFF > 0.050)
5. To'liq shaxmat dvigateli orqali qonuniy yurishlarni hisoblaydi
6. Taxta, kursor, sudrab olib yurish va UI elementlarini chizadi

Shaxmat dvigateli quyidagilarni o'z ichiga oladi:

- Barcha figuralar yurish mantig'i (piyoda, ot, fil, rux, farzin, shoh)
- Sliding figuralar uchun nur otish
- Shoxni aniqlash
- Qonuniy yurishlarni filtrlash (shox ostida qoladigan yurishlarni bloklash)
- Shox-mat va patni aniqlash
- Piyodani avtomatik farzinga aylantirish

---

## 🖼️ Skrinshotlar

<details>
<summary>Ko'rish uchun bosing</summary>

— *Skrinshotlar tez orada* —

</details>

---

## 🧪 Brauzer qo'llab-quvvatlashi

| Brauzer | Holati |
|---------|--------|
| Chrome | ✅ To'liq qo'llab-quvvatlanadi |
| Firefox | ✅ Qo'llab-quvvatlanadi |
| Safari | ⚠️ Localhost talab qilinishi mumkin |
| Edge | ✅ Qo'llab-quvvatlanadi |

