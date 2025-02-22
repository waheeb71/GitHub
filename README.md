# أوامر Git الأساسية والمهمة لرفع المشاريع إلى GitHub

## الأوامر الأساسية:

1. **تهيئة المستودع** (إنشاء مستودع Git محلي):
   ```bash
   git init
   ```

2. **إضافة الملفات إلى المستودع** (إضافة جميع الملفات إلى مرحلة الإعداد):
   ```bash
   git add .
   ```

3. **حفظ التغييرات** (إنشاء نقطة استعادة - Commit):
   ```bash
   git commit -m "Initial commit"
   ```

4. **إنشاء فرع رئيسي**:
   ```bash
   git branch -M main
   ```

5. **ربط المستودع المحلي مع GitHub**:
   ```bash
   git remote add origin <رابط المستودع>
   ```
   🔹 استبدل `<رابط المستودع>` بالرابط الفعلي لمشروعك على GitHub.

6. **رفع المشروع لأول مرة إلى GitHub**:
   ```bash
   git push -u origin main
   ```

7. **رفع التحديثات بعد التعديل**:
   ```bash
   git push origin main
   ```

---

## الأوامر الاختيارية والمفيدة:

1. **معرفة حالة المستودع**:
   ```bash
   git status
   ```

2. **مشاهدة تاريخ التعديلات بشكل مختصر**:
   ```bash
   git log --oneline --graph --all
   ```

3. **سحب التحديثات من المستودع البعيد** (في حال وجود تعديلات جديدة على GitHub):
   ```bash
   git pull origin main
   ```

4. **إعادة تعيين المستودع (في حال حدوث مشاكل)**:
   ```bash
   git reset --hard HEAD
   ```

5. **معرفة الإصدارات المتاحة (عرض سجل التعديلات)**:
   ```bash
   git log --oneline
   ```

6. **إلغاء آخر commit فقط (إذا لم يتم رفعه إلى GitHub بعد)**:
   ```bash
   git reset --soft HEAD~1
   ```

7. **التراجع عن آخر commit وحذف الملفات أيضًا**:
   ```bash
   git reset --hard HEAD~1
   ```

8. **تحميل مشروع من GitHub**:
   ```bash
   git clone <رابط المستودع>
   ```
   🔹 استبدل `<رابط المستودع>` بالرابط الفعلي للمشروع الذي تريد تحميله.

---

# أوامر Git الأساسية والمهمة لرفع المشاريع إلى GitHub

## الأوامر الأساسية:

1. **تهيئة المستودع** (إنشاء مستودع Git محلي):
   ```bash
   git init
   ```

2. **إضافة الملفات إلى المستودع** (إضافة جميع الملفات إلى مرحلة الإعداد):
   ```bash
   git add .
   ```

3. **حفظ التغييرات** (إنشاء نقطة استعادة - Commit):
   ```bash
   git commit -m "Initial commit"
   ```

4. **إنشاء فرع رئيسي**:
   ```bash
   git branch -M main
   ```

5. **ربط المستودع المحلي مع GitHub**:
   ```bash
   git remote add origin <رابط المستودع>
   ```
   🔹 استبدل `<رابط المستودع>` بالرابط الفعلي لمشروعك على GitHub.

6. **رفع المشروع لأول مرة إلى GitHub**:
   ```bash
   git push -u origin main
   ```

7. **رفع التحديثات بعد التعديل**:
   ```bash
   git push origin main
   ```

---

## الأوامر الاختيارية والمفيدة:

1. **معرفة حالة المستودع**:
   ```bash
   git status
   ```

2. **مشاهدة تاريخ التعديلات بشكل مختصر**:
   ```bash
   git log --oneline --graph --all
   ```

3. **سحب التحديثات من المستودع البعيد** (في حال وجود تعديلات جديدة على GitHub):
   ```bash
   git pull origin main
   ```

4. **إعادة تعيين المستودع (في حال حدوث مشاكل)**:
   ```bash
   git reset --hard HEAD
   ```

5. **معرفة الإصدارات المتاحة (عرض سجل التعديلات)**:
   ```bash
   git log --oneline
   ```

6. **إلغاء آخر commit فقط (إذا لم يتم رفعه إلى GitHub بعد)**:
   ```bash
   git reset --soft HEAD~1
   ```

7. **التراجع عن آخر commit وحذف الملفات أيضًا**:
   ```bash
   git reset --hard HEAD~1
   ```

8. **تحميل مشروع من GitHub**:
   ```bash
   git clone <رابط المستودع>
   ```
   🔹 استبدل `<رابط المستودع>` بالرابط الفعلي للمشروع الذي تريد تحميله.

---

## إعداد Git باستخدام SSH:

1. **إنشاء مفتاح SSH جديد**:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
   ```
   🔹 استبدل `your-email@example.com` ببريدك الإلكتروني المسجل في GitHub.

2. **نسخ المفتاح إلى الحافظة (على Windows)**: 
   ```bash
   clip < ~/.ssh/id_rsa.pub
   ```

3. **التحقق من وجود مفتاح SSH**:
   ```bash
   dir ~/.ssh
   ```

4. **اختبار الاتصال بـ GitHub عبر SSH**:
   ```bash
   ssh -T git@github.com
   ```

5. **تحديث عنوان المستودع لاستخدام SSH بدلاً من HTTPS**:
   ```bash
   git remote set-url origin git@github.com:your-username/your-repo.git
   ```
استبدله باسم المستخدم الخاص فيك واسم المشروع your-username/your-repo.git

6. **رفع المشروع لأول مرة إلى GitHub**:
   ```bash
   git push -u origin main
   ```

7. **رفع التحديثات بعد التعديل**:
   ```bash
   git push origin main
   ```

   
---

## أوامر إضافية مفيدة:

1. **تعطيل تحويل تنسيق الأسطر (لمنع مشاكل التوافق بين Windows وLinux)**:
   ```bash
   git config --global core.autocrlf false
   ```

2. **جلب جميع التحديثات من المستودع البعيد**:
   ```bash
   git fetch --all
   ```

3. **إعادة تعيين الكود إلى آخر تحديث في المستودع البعيد**:
   ```bash
   git reset --hard origin/main
   ```

4. **رفع المشروع بعد إعداد SSH**:
   ```bash
   git push -u origin main
   ```

---

📌 **ملاحظة**: تأكد من أنك مسجل دخولك إلى GitHub باستخدام `git config` أو عبر `SSH` لضمان عدم وجود مشاكل عند رفع الملفات أو تحميلها.

🚀 **بالتوفيق في مشاريعك على GitHub!**





