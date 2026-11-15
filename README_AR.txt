YAFINO FRUITS - نسخة لوحة المالك

محتويات المشروع:
- index.html: واجهة المتجر ولوحة المالك.
- netlify/functions: تسجيل الدخول وقراءة/حفظ المنتجات على الخادم.
- netlify.toml و package.json: إعدادات نشر Netlify.

مهم جداً:
هذه النسخة تحتاج نشر Netlify مع تشغيل Netlify Functions. لا ترفعها عبر Netlify Drop كملفات ثابتة؛ الرفع الثابت وحده لا يشغّل وظائف الخادم.

إعدادات Netlify المطلوبة بعد ربط المشروع بمستودع Git:
Build command: npm install
Publish directory: .

أضف متغيري البيئة في Project configuration > Environment variables:
ADMIN_PASSWORD = كلمة مرور قوية تختارها أنت ولا ترسلها لأحد.
SESSION_SECRET = قيمة عشوائية سرية لا تقل عن 32 حرفاً.

بعد إضافة المتغيرات، أعد نشر الموقع (Trigger deploy / Clear cache and deploy).

رابط لوحة المالك بعد النشر:
https://رابط-متجرك/#owner

رابط الزبائن:
https://رابط-متجرك/

المنتجات الحالية تبقى ظاهرة من HTML أول مرة. عند أول حفظ من لوحة المالك تُخزّن القائمة في Netlify Blobs، وبعد ذلك تُحمّل للزبائن من الخادم.
