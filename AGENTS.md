# Mg6 — MiniPC OS (نظام تشغيل مصغر)

تطبيق Android (WebView) يعرض نظام تشغيل مصغر HTML5 يحتوي على 12+ تطبيقًا.

## البناء
يتم البناء تلقائيًا على GitHub Actions عند كل push إلى `main`.
- الـ workflow: `.github/workflows/build-apk.yml`
- الناتج: `android/app/build/outputs/apk/debug/app-debug.apk` (تحميله من تبويب Actions → Artifacts)

## البناء محليًا (اختياري)
```bash
cd android && gradle assembleDebug --no-daemon
```

## الملفات
- `android/` — مشروع Android (Gradle Kotlin DSL)
- `android/app/src/main/java/com/musab/mg6/MainActivity.java` — WebView يحمّل الواجهة
- `android/app/src/main/assets/www/index.html` — نظام MiniPC OS (ملف واحد)
