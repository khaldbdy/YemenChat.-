# YemenChat 🇾🇪

**تطبيق مراسلة فورية شبيه بـ WhatsApp**

Developed & Designed by **Khaled Badeer**

---

## 📱 المميزات

- ✅ تسجيل دخول برقم الهاتف (OTP) - اليمن (+967) افتراضياً
- ✅ محادثات فورية في الوقت الحقيقي
- ✅ إرسال نصوص وصور
- ✅ مؤشر الكتابة (Typing indicator)
- ✅ حالة الاتصال (متصل/غير متصل)
- ✅ حالة الرسالة (مرسلة ✓ / تم التسليم ✓✓ / مقروءة ✓✓ أزرق)
- ✅ إشعارات (Firebase Cloud Messaging)
- ✅ الوضع الداكن 🌙
- ✅ دعم RTL كامل (العربية)
- ✅ حذف الرسائل (لي / للجميع)
- ✅ مزامنة جهات الاتصال
- ✅ تصميم Material Design 3

---

## 🔧 الإعداد

### 1. Firebase

1. أنشئ مشروع في [Firebase Console](https://console.firebase.google.com)
2. فعّل **Authentication → Phone** provider
3. فعّل **Cloud Firestore**
4. فعّل **Realtime Database**
5. فعّل **Cloud Storage**
6. فعّل **Cloud Messaging**
7. حمّل `google-services.json` وضعه في مجلد `app/`

### 2. قواعد الأمان

- انسخ `firestore.rules` إلى Firestore Rules
- انسخ `database.rules.json` إلى Realtime Database Rules
- انسخ `storage.rules` إلى Storage Rules

### 3. البناء

```bash
# Android Studio
./gradlew assembleDebug

# AIDE
# افتح المجلد مباشرة في AIDE
```

---

## 📁 هيكل المشروع

```
com.khaledbadeer.yemenchat/
├── activities/        # شاشات التطبيق
├── adapters/          # محولات RecyclerView
├── firebase/          # خدمات Firebase
├── fragments/         # الأجزاء (تبويبات)
├── models/            # نماذج البيانات
└── utils/             # أدوات مساعدة
```

---

## 📦 التبعيات

- Firebase (Auth, Firestore, Realtime DB, Storage, FCM)
- Glide (تحميل الصور)
- CircleImageView
- CountryCodePicker
- Material Design 3

---

## 🏗️ قاعدة البيانات

### Firestore
- `users/{uid}` — بيانات المستخدم
- `chats/{chatId}` — بيانات المحادثة
- `chats/{chatId}/messages/{msgId}` — الرسائل
- `status/{statusId}` — القصص

### Realtime Database
- `presence/{uid}` — حالة الاتصال
- `typing/{chatId}/{uid}` — مؤشر الكتابة

---

## ⚠️ ملاحظة

ضع ملف `google-services.json` في مجلد `app/` قبل البناء.

---

**© 2024 Khaled Badeer - جميع الحقوق محفوظة**
