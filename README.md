# CV Chess — Qo'l bilan boshqariladigan shaxmat

**CV Chess** — bu kamerangiz orqali qo'l harakatlari bilan boshqariladigan interaktiv shaxmat o'yini. MediaPipe Hands texnologiyasi yordamida barmoq holati aniqlanadi va shaxmat taxtasida real vaqt rejimida harakatlanadi.

## Texnologiyalar

- **MediaPipe Hands** — qo'l va barmoq holatini aniqlash
- **Vanilla JavaScript** — o'yin logikasi va UI
- **CSS Grid** — responsiv shaxmat taxtasi

## Ishga tushirish

Mahalliy server orqali ishga tushiring:

```bash
python -m http.server 8000
```

So'ng brauzerda oching: `http://localhost:8000`

> Web-kamera ishlashi uchun **localhost** yoki **HTTPS** talab qilinadi.

## Foydalanish

1. **"Kamerani yoqish"** tugmasini bosing va kameraga ruxsat bering
2. Ko'rsatkich barmog'ingiz bilan shaxmat taxtasida yuring
3. Piyodani ushlash uchun barmoqni **chimching** (bosh va ko'rsatkich barmoqni birlashtiring)
4. Yurishni amalga oshirish uchun chimchishni **bo'shating**

## Xususiyatlar

- To'liq shaxmat qoidalari (barcha figuralar, shox, shox-mat)
- Qo'l tracking orqali intuitiv boshqaruv
- Real vaqt rejimida debug paneli
- Avtomatik piyodani qirolichaga aylantirish
- Responsiv dizayn

## Litsenziya

MIT
