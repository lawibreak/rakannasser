# مدونة راكان ناصر

مدونة ثابتة مبنية بـ Jekyll وتُستضاف مجانًا على GitHub Pages.

## النشر على GitHub Pages

1. أنشئ مستودعًا جديدًا على GitHub (مثلًا `blog`) وارفع هذه الملفات إليه.
2. من المستودع: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / **(root)**
3. بعد دقيقة أو اثنتين تظهر المدونة على:
   - `https://<اسم-المستخدم>.github.io/blog/` — وفي هذه الحالة عدّل `baseurl: "/blog"` في `_config.yml`.
   - أو سمِّ المستودع `<اسم-المستخدم>.github.io` لتكون على الجذر مباشرة واترك `baseurl` فارغًا.
4. لربط نطاق خاص: **Settings → Pages → Custom domain**.

## إضافة تدوينة

أنشئ ملفًا في `_posts/` باسم `YYYY-MM-DD-عنوان-قصير.md`:

```markdown
---
title: عنوان التدوينة
date: 2026-10-19
image: /assets/img/cover.png   # اختياري
tags: [مدونة]
excerpt: سطر يظهر في المشاركات ونتائج البحث.
---

نص التدوينة بصيغة Markdown…

## عنوان فرعي

**خط عريض**، *مائل*.

> اقتباس
```

ضع الصور في `assets/img/`.

## إضافة شذرة

أنشئ ملفًا في `_notes/` باسم `YYYY-MM-DD-اسم.md`:

```markdown
---
date: 2026-10-19
type: رابط        # خاطرة | رابط | يوتيوب | كتاب | فيلم
link: https://…   # اختياري
image: /assets/img/thumb.jpg   # اختياري
---

نص الشذرة.
```

## ملفات أخرى

| الملف | الغرض |
|---|---|
| `_config.yml` | الاسم، الوصف، روابط التواصل، التعليقات |
| `about.md` | صفحة «عنّي» |
| `_data/books.yml` | الإصدارات وروابط الشراء/التحميل |
| `assets/css/style.css` | الألوان والتصميم (المتغيرات في أعلى الملف) |

## التعليقات (اختياري)

فعّل [Giscus](https://giscus.app) على المستودع ثم انسخ القيم إلى قسم `giscus` في `_config.yml`.

## المعاينة محليًا

يتطلب Ruby 3:

```bash
bundle install
bundle exec jekyll serve
```

ثم افتح http://localhost:4000
