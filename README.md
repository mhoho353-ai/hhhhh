# hhhhh
# 🎨 ImageAI — مولّد صور مجاني (PWA)

تطبيق ويب تقدمي (PWA) لتوليد صور بالذكاء الاصطناعي مجاناً عبر Hugging Face Inference API.

---

## 📁 ملفات المشروع

```
index.html     ← التطبيق الكامل (HTML + CSS + JS في ملف واحد)
manifest.json  ← إعدادات PWA (الاسم، الأيقونة، الألوان)
sw.js          ← Service Worker (يحفظ الكاش ويشغّل أوفلاين)
icon.svg       ← أيقونة التطبيق
README.md      ← هذا الملف
```

---

## 🚀 النشر على Vercel (مجاني 100%)

### من الهاتف خطوة بخطوة:

**1. GitHub**
- افتح github.com → سجّل حساباً مجانياً
- اضغط "+" → "New repository"
- الاسم: `imageai` ← Public ← Create
- ارفع الملفات الأربعة: index.html، manifest.json، sw.js، icon.svg

**2. Vercel**
- افتح vercel.com → Continue with GitHub
- Add New Project → اختر repo الـ `imageai`
- اضغط Deploy ← ينتهي في 30 ثانية!
- ستحصل على رابط مثل: `imageai.vercel.app`

**3. تثبيت كتطبيق**

أندرويد (Chrome):
- افتح الرابط ← ستظهر رسالة "Install App" تلقائياً
- أو: القائمة ⋮ ← "Add to Home Screen"

iPhone (Safari فقط):
- افتح الرابط في Safari ← زر المشاركة ⬆️ ← "Add to Home Screen"

---

## 🔑 الحصول على مفتاح API المجاني

1. سجّل في https://huggingface.co/join (مجاني، لا يحتاج بطاقة)
2. اذهب إلى https://huggingface.co/settings/tokens
3. "New token" → النوع: "Read" → أنشئ → انسخ المفتاح (يبدأ بـ hf_)
4. افتح التطبيق → "ربط API" → الصق المفتاح

---

## 🧠 النماذج المدمجة المجانية

| النموذج | الجودة | السرعة | الرابط |
|---------|--------|--------|--------|
| FLUX.1 Schnell | ⭐⭐⭐⭐ | ⚡ سريع جداً | https://huggingface.co/black-forest-labs/FLUX.1-schnell |
| FLUX.1 Dev | ⭐⭐⭐⭐⭐ | متوسط | https://huggingface.co/black-forest-labs/FLUX.1-dev |
| SDXL Base 1.0 | ⭐⭐⭐⭐ | متوسط | https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0 |
| Stable Diffusion 2.1 | ⭐⭐⭐ | سريع | https://huggingface.co/stabilityai/stable-diffusion-2-1 |
| DreamShaper 8 | ⭐⭐⭐⭐ | سريع | https://huggingface.co/Lykon/dreamshaper-8 |
| SD 1.5 Classic | ⭐⭐⭐ | سريع جداً | https://huggingface.co/runwayml/stable-diffusion-v1-5 |

---

## 🛠️ أخطاء شائعة وحلها

| الخطأ | السبب | الحل |
|-------|-------|------|
| 503 | النموذج يُحمَّل | انتظر 30-60 ث وأعد المحاولة |
| 401 | مفتاح خاطئ | تحقق من المفتاح |
| 402 | تجاوزت الحد المجاني | انتظر تجديد الشهر |
| 429 | طلبات كثيرة | انتظر دقيقة |
| 422 | النموذج لا يدعم API | اختر نموذجاً آخر |

---

## ✨ مميزات التطبيق

- ✅ مجاني 100% (HuggingFace + Vercel)
- ✅ يعمل كتطبيق PWA على iOS وأندرويد
- ✅ يحفظ آخر صورة تلقائياً
- ✅ تحميل الصور بضغطة واحدة
- ✅ مشاركة الصور (Web Share API)
- ✅ 6 نماذج مدمجة + إضافة نماذج مخصصة
- ✅ يعمل بدون إنترنت (Service Worker)
- ✅ واجهة عربية RTL بالكامل
- ✅ لا يرسل مفتاحك لأي خادم غير HuggingFace
