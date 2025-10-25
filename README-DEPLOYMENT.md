# 🚀 دليل نشر المشروع

## 📋 **الطرق المتاحة للنشر:**

### **1. النشر المحلي (Local Network)**

#### **أ) استخدام Python Server:**
```bash
# انتقل إلى مجلد المشروع
cd restaurant-dashboard

# شغل الخادم
python -m http.server 8000

# أو للوصول من الشبكة المحلية
python -m http.server 8000 --bind 0.0.0.0
```

**الوصول للموقع:**
- **من جهازك**: `http://localhost:8000`
- **من أجهزة أخرى**: `http://YOUR_IP:8000`

#### **ب) استخدام Node.js Live Server:**
```bash
# تثبيت Live Server
npm install -g live-server

# شغل الخادم
npx live-server restaurant-dashboard --port=8000 --host=0.0.0.0
```

### **2. النشر على الإنترنت**

#### **أ) GitHub Pages (مجاني):**

1. **إنشاء مستودع GitHub:**
   - اذهب إلى [GitHub.com](https://github.com)
   - أنشئ مستودع جديد باسم `restaurant-dashboard`
   - اختر "Public" للوصول المجاني

2. **رفع الملفات:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/restaurant-dashboard.git
   git push -u origin main
   ```

3. **تفعيل GitHub Pages:**
   - اذهب إلى Settings > Pages
   - اختر Source: Deploy from a branch
   - اختر Branch: main
   - اضغط Save

4. **الوصول للموقع:**
   - `https://YOUR_USERNAME.github.io/restaurant-dashboard`

#### **ب) Netlify (مجاني وسهل):**

1. **رفع الملفات:**
   - اذهب إلى [Netlify.com](https://netlify.com)
   - اسحب مجلد `restaurant-dashboard` إلى منطقة النشر
   - أو اربط مع GitHub repository

2. **الوصول للموقع:**
   - ستحصل على رابط مثل: `https://amazing-name-123456.netlify.app`

#### **ج) Vercel (مجاني وسريع):**

1. **رفع الملفات:**
   - اذهب إلى [Vercel.com](https://vercel.com)
   - اربط مع GitHub أو ارفع الملفات مباشرة

2. **الوصول للموقع:**
   - ستحصل على رابط مثل: `https://restaurant-dashboard.vercel.app`

### **3. النشر على خادم خاص**

#### **أ) استخدام Apache/Nginx:**
- ارفع الملفات إلى مجلد `public_html`
- تأكد من أن `index.html` في المجلد الرئيسي
- الوصول عبر: `https://yourdomain.com`

#### **ب) استخدام Node.js:**
```bash
# تثبيت PM2 لإدارة العمليات
npm install -g pm2

# شغل المشروع
pm2 start "npx live-server restaurant-dashboard --port=80" --name "restaurant-dashboard"
```

## 🔐 **إدارة المستخدمين:**

### **كمدير:**
1. **تسجيل الدخول:** استخدم كلمة المرور من `config.js`
2. **إضافة مطاعم:** اضغط على "إضافة مطعم جديد"
3. **تحديث البيانات:** اضغط على "تحديث البيانات"
4. **إدارة الإعدادات:** اذهب إلى قسم الإعدادات

### **للمستخدمين العاديين:**
1. **عرض المطاعم:** تصفح قائمة المطاعم
2. **البحث السريع:** استخدم البحث للعثور على المناطق
3. **عرض التفاصيل:** اضغط على أي مطعم لرؤية التفاصيل
4. **لا يمكنهم إضافة مطاعم:** فقط العرض والبحث

## 📱 **الوصول من الهواتف:**

### **من الشبكة المحلية:**
- تأكد من أن جميع الأجهزة على نفس الشبكة
- استخدم عنوان IP الخاص بك
- مثال: `http://192.168.1.100:8000`

### **من الإنترنت:**
- استخدم الرابط الذي حصلت عليه من GitHub Pages/Netlify/Vercel
- يعمل على جميع الأجهزة والهواتف
- لا حاجة لشبكة محلية

## 🛠️ **نصائح مهمة:**

1. **تغيير كلمة المرور:** عدل `ADMIN.PASSWORD` في `config.js`
2. **النسخ الاحتياطي:** احفظ نسخة من البيانات المهمة
3. **التحديث:** أعد رفع الملفات عند التحديث
4. **الأمان:** استخدم HTTPS في الإنتاج

## 📞 **الدعم:**

إذا واجهت أي مشاكل:
1. تأكد من أن جميع الملفات موجودة
2. تحقق من عنوان URL
3. تأكد من اتصال الإنترنت
4. جرب متصفح مختلف


