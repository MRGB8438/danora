[README.md](https://github.com/user-attachments/files/32239289/README.md)
# danora<div dir="rtl">

# 🎓 دانورا (DANORA)

**سیستم‌عامل دانشجویی — همراه هوشمند تو در مسیر دانایی و پیشرفت**

دانورا یک اپلیکیشن کامل مدیریت زندگی دانشگاهی است: برنامه هفتگی، حضور و غیاب، وظایف و پروژه‌ها، نمرات و معدل، جزوه‌نویسی، تایمر تمرکز، گزارش هفتگی عملکرد، قفل برنامه با اثر انگشت و خیلی چیزهای دیگر — همه در یک اپ زیبا، فارسی و کاملاً آفلاین.

<p align="center">
  <img src="https://img.shields.io/badge/نسخه-1.0.0-3b6eff?style=for-the-badge" alt="version" />
  <img src="https://img.shields.io/badge/Android-7.0%2B-3ddc84?style=for-the-badge&logo=android" alt="android" />
  <img src="https://img.shields.io/badge/PWA-%F0%9F%94%97-5a0fc8?style=for-the-badge" alt="pwa" />
  <img src="https://img.shields.io/badge/React_18-TypeScript-149eca?style=for-the-badge&logo=react" alt="react" />
</p>

</div>

---

<div dir="ltr">

## ✨ Why DANORA?

DANORA is a **privacy-first student operating system**. Everything runs 100% on your device — no account, no server, no tracking. Built with love for Iranian university students, fully in Persian (RTL) with a beautiful dark UI.

## 🚀 Get Started

**Android** — grab the latest APK from [Releases](https://github.com/MRGB8438/danora/releases) and install it directly (allow "Install unknown apps" when asked).

**Web (PWA)** — host the static `dist` build on any free static host (Netlify / Cloudflare Pages / GitHub Pages), open it in Chrome and tap **"Add to Home screen"**. Full step-by-step deployment guide: `danora-deploy-guide-fa.pdf` (Persian).

**In-app updates** — DANORA checks GitHub Releases every 6 hours (and manually from *Settings → Update*). When you publish a release with a higher `vX.Y.Z` tag and an APK asset, every user gets an update banner with a direct download link.

## 🧩 Feature Highlights

| Area | What you get |
|---|---|
| 📅 Academic | Weekly schedule, courses & professors, exams & projects with countdowns, calendar |
| ✅ Productivity | Tasks with priorities, focus timer (Pomodoro-style), weekly performance report |
| 📊 Grades | Grade tracker, weighted GPA calculator, attendance tracker with skip limits |
| 📝 Notes | Lecture notebook (rich blocks), files manager, PDF/image viewers |
| 🤖 AI | Built-in AI assistant center (bring your own API key) |
| 🔒 Security | App lock with PIN + fingerprint (Android biometrics), auto-relock in background |
| 💾 Data | 100% local storage, automatic scheduled backups, one-tap backup/restore, export |
| 🎨 Personalize | Dark/light themes, accent colors, animated star backgrounds, student ID card |
| 🔄 Updates | GitHub-releases-based updater, PWA service-worker auto-update |

</div>

---

<div dir="rtl">

## 🧩 امکانات به فارسی

- **برنامه هفتگی و درس‌ها** — جدول کلاس‌ها با استاد، واحد، محل کلاس و یادآور قبل از کلاس
- **وظایف، پروژه‌ها و امتحانات** — اولویت‌بندی، شمارش معکوس، اعلان‌های هوشمند
- **حضور و غیاب** — ثبت حضور/غیبت/مجاز با سقف غیبت و هشدار قبل از رسیدن به مرز خطر
- **نمرات و معدل** — ثبت نمره با وزن واحد، محاسبه معدل ترم و کل، ذخیره محاسبات
- **جزوه‌نویسی** — دفترچه یادداشت بلوکی برای هر درس + مدیریت فایل‌ها (PDF، عکس، سند)
- **تایمر تمرکز** — تمرکز عمیق با ثبت آمار، همراه با گزارش هفتگی
- **گزارش هفتگی عملکرد** — تصویر هفته تو در یک نگاه: تمرکز، وظایف، حضور، نمرات و رویدادها
- **قفل برنامه** — پین + اثر انگشت (بیومتریک اندروید)، قفل خودکار هنگام رفتن به پس‌زمینه
- **دستیار هوش مصنوعی** — چت هوشمند دانشگاهی با کلید API خودت
- **پشتیبان‌گیری** — خودکار زمان‌بندی‌شده + دستی، روی حافظه گوشی یا خروجی فایل JSON
- **آپدیت خودکار** — چک هر ۶ ساعت از Releases همین مخزن + بنر «نسخه جدید» با دانلود مستقیم
- **PWA** — نسخه وب قابل نصب روی گوشی و دسکتاپ، کاملاً آفلاین پس از نصب اولیه

## 🔐 حریم خصوصی

دانورا **هیچ سروری ندارد**. همه داده‌ها (نمرات، عکس‌ها، جزوه‌ها، پروفایل و…) فقط روی دستگاه خودت ذخیره می‌شوند. تنها ارتباط شبکه‌ای برنامه، چک‌کردن Releases گیت‌هاب برای آپدیت است.

## 🛠 ساخت از سورس

<div dir="ltr">

```bash
# prerequisites: Node 18+, JDK 21, Android SDK (for the Android build)

git clone https://github.com/MRGB8438/danora.git
cd danora
npm install

# web / PWA build → dist/
npm run build

# android APK + AAB
npx cap sync android
cd android
./gradlew assembleRelease bundleRelease
# outputs: app/build/outputs/apk/release/app-release.apk
#          app/build/outputs/bundle/release/app-release.aab
```

</div>

## 🔄 انتشار نسخه جدید (برای مالک مخزن)

<div dir="ltr">

1. Bump the version: `package.json`, `android/app/build.gradle` (`versionName` + `versionCode`) and `APP_VERSION` in `src/lib/updater.ts`.
2. Build the release APK, then go to **Releases → Draft a new release**.
3. Tag it `vX.Y.Z` (must be **greater** than the current app version) and attach the APK file.
4. Users get the update banner automatically within 6 hours (or instantly via *Check for update*).

</div>

## 📱 فناوری‌ها

<div dir="ltr">

| Layer | Tech |
|---|---|
| UI | React 18 · TypeScript · Tailwind CSS · lucide-react |
| Core | Vite 5 · vite-plugin-pwa (Workbox) |
| Native | Capacitor 7 (Android) · custom BiometricPlugin (framework BiometricPrompt) |
| Docs/Export | jsPDF · SheetJS (xlsx) · qrcode |

</div>

## ⚠️ نکته نصب اندروید

چون برنامه خارج از گوگل‌پلی نصب می‌شود، ممکن است **Play Protect** هشدار بدهد. گزینه «نصب در هر صورت (Install anyway)» را بزن؛ این هشدار برای همه اپ‌های منتشرشده خارج از پلی است و نشانه مشکلی در دانورا نیست.

## 📄 لایسنس

© MRGB8438 — ساخته‌شده با ❤️ برای دانشجوهای ایران

</div>
