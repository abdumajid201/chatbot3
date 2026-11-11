# Telegram AI javob bot

Node.js orqali shaxsiy Telegram chatlaridagi matnli xabarlarga Google Gemini API yordamida javob tayyorlaydigan boshlang‘ich loyiha.

## Ishga tushirish

1. Node.js 20.6 yoki yangirog‘ini o‘rnating.
2. Telegramda [@BotFather](https://t.me/BotFather) orqali yangi bot yarating va token oling.
3. [Google AI Studio](https://aistudio.google.com/app/apikey) orqali Gemini API kalitini oling.
4. `.env.example` faylidan `.env` nusxa yarating va `TELEGRAM_BOT_TOKEN`, `GEMINI_API_KEY` hamda ismingizni kiriting.
5. Terminalda `npm start` buyrug‘ini bajaring.
6. Telegramda yangi botni ochib `/start` yuboring.


Gemini API bepul darajasida so‘rovlar soni va tezligiga cheklovlar bor; amaldagi limitlar AI Studio hisobingizda ko‘rinadi. Bepul darajadagi kontent Google mahsulotlarini yaxshilash uchun ishlatilishi mumkin, shu sabab botga maxfiy yoki nozik ma’lumotlarni yubormang.

## Renderga bepul joylash

1. Loyihani GitHub repositoryga yuklang. `.gitignore` `.env` faylini chiqarib tashlaydi; maxfiy kalitlarni GitHubga yubormang.
2. Render Dashboard’da **New → Blueprint** ni tanlab, repositoryni ulang. Render `render.yaml` sozlamasini o‘qiydi.
3. So‘ralganda `TELEGRAM_BOT_TOKEN` va `GEMINI_API_KEY` qiymatlarini Render’ning Environment bo‘limiga kiriting. Webhook himoya siri avtomatik yaratiladi.
4. **Free** rejadagi xizmatni deploy qiling. Xizmat ishga tushganda Telegram webhook manzilini o‘zi ro‘yxatdan o‘tkazadi.

Render Free 15 daqiqa kiruvchi trafik bo‘lmasa xizmatni uxlatadi; keyingi xabarda uyg‘onishi taxminan bir daqiqa olishi mumkin. Bu botni bepul sinash uchun mos, javoblar doimiy ravishda tez bo‘lishini kafolatlamaydi. Render’da bot ishlayotgan paytda shu token bilan lokal `npm start` ni parallel ishlatmang — Telegram bitta update qabul qilish usulini qo‘llaydi.
## Buyruqlar

- `/start` — bot bilan boshlash.
- `/reset` — shu chatning vaqtinchalik suhbat xotirasini tozalash.

Suhbat xotirasi hozircha faqat dastur ishlayotgan paytda saqlanadi; restartdan keyin yo‘qoladi. Bot faqat shaxsiy chatlardagi matnli xabarlarga javob beradi. Guruh xabarlari va media hali yoqilmagan.

Bot alohida Telegram bot akkaunti sifatida ko‘rinadi. U sizning shaxsiy akkauntingiz bo‘lib ko‘rinmaydi. Xabarlar javob olish uchun Google Gemini API’ga yuboriladi.
