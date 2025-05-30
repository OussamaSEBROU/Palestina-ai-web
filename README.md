# Palestina-ai - منصة دعم القضية الفلسطينية

Palestina-ai هي منصة متكاملة مبنية باستخدام Django وتهدف إلى دعم القضية الفلسطينية من خلال تقديم محتوى حصري ودقيق حول فلسطين، مع واجهة احترافية وعصرية، ودعم كامل للغة العربية.

## الميزات الرئيسية

- **محادثة ذكية**: محادثة تفاعلية مع مساعد ذكي متخصص في القضية الفلسطينية باستخدام Gemini API
- **توليد الصور**: إنشاء صور داعمة للقضية الفلسطينية باستخدام Gemini API
- **مقالات متخصصة**: محتوى معمق حول تاريخ فلسطين والتطورات الحديثة
- **بيانات اقتصادية**: عرض أحدث البيانات الاقتصادية عن فلسطين باستخدام DataBank API
- **طرق الدعم**: اقتراح طرق عملية لدعم القضية الفلسطينية
- **سجل المحادثات**: حفظ وعرض سجل المحادثات السابقة مع إمكانية البحث
- **واجهة متجاوبة**: تصميم يناسب جميع الأجهزة (الحواسيب، الهواتف، الأجهزة اللوحية)
- **سمات متعددة**: دعم الوضع الفاتح والداكن مع استخدام ألوان العلم الفلسطيني

## المتطلبات التقنية

- Python 3.10+
- Django 5.2+
- Gemini API
- وصول إلى الإنترنت للتفاعل مع واجهات برمجة التطبيقات الخارجية

## التثبيت

1. استنساخ المستودع:
```bash
git clone https://github.com/yourusername/palestina-ai.git
cd palestina-ai
```

2. إنشاء بيئة افتراضية وتفعيلها:
```bash
python -m venv venv
source venv/bin/activate  # على Linux/Mac
# أو
venv\Scripts\activate  # على Windows
```

3. تثبيت المتطلبات:
```bash
pip install -r requirements.txt
```

4. إعداد متغيرات البيئة:
```bash
export GEMINI_API_KEY=your_api_key_here
# أو على Windows
set GEMINI_API_KEY=your_api_key_here
```

5. تطبيق الترحيلات:
```bash
python manage.py migrate
```

6. جمع الملفات الثابتة:
```bash
python manage.py collectstatic
```

7. تشغيل الخادم:
```bash
python manage.py runserver
```

8. الوصول إلى التطبيق على العنوان: http://localhost:8000

## الإعدادات

يمكن تعديل الإعدادات في ملف `palestina_ai/settings.py`:

- `DEBUG`: يجب تعيينه إلى `False` في بيئة الإنتاج
- `SECRET_KEY`: يجب تغييره إلى مفتاح قوي وفريد في بيئة الإنتاج
- `ALLOWED_HOSTS`: يجب تحديده بقائمة النطاقات المسموح بها في بيئة الإنتاج
- `GEMINI_API_KEY`: مفتاح API لخدمة Gemini
- `GEMINI_TEXT_MODEL`: نموذج Gemini المستخدم لتوليد النصوص
- `GEMINI_IMAGE_MODEL`: نموذج Gemini المستخدم لتوليد الصور

## هيكل المشروع

- `core`: التطبيق الأساسي (الصفحة الرئيسية، عن القضية، طرق الدعم)
- `chat`: تطبيق المحادثة وسجل المحادثات
- `articles`: تطبيق المقالات والتصنيفات
- `api`: واجهة برمجة التطبيقات للتفاعل مع Gemini API وDataBank API
- `templates`: قوالب HTML
- `static`: الملفات الثابتة (CSS، JavaScript، الصور)
- `media`: الملفات المرفوعة (الصور المولدة، صور المقالات)

## التحسينات والتطوير

تم تحسين الأداء من خلال:
- إضافة فهارس لتحسين استعلامات قاعدة البيانات
- تحسين الأمان وفقًا لأفضل ممارسات Django
- تحسين تحميل الملفات الثابتة

## الترخيص

هذا المشروع مرخص بموجب رخصة MIT. انظر ملف LICENSE للحصول على التفاصيل.

## المساهمة

نرحب بالمساهمات! يرجى إرسال طلبات السحب أو فتح مشكلات لتحسين المشروع.

---

تم تطويره بواسطة فريق Palestina-ai لدعم القضية الفلسطينية.
