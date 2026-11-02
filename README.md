# ALHami Download Manager

مدير تحميل مفتوح المصدر لنظام Windows. يهدف ALHami إلى توفير وظائف إدارة التنزيلات والاستكمال والتكامل مع المتصفحات، انطلاقًا من مشروع [Zajil Download Manager](https://github.com/motalim-ai/zajil-download-manager).

**المشروع قيد إعادة الهوية والتحقق. لا توجد نسخة ALHami جاهزة للتنزيل أو التحديث بعد.** لا تستخدم إصدارات Zajil لتثبيت ALHami أو تحديثه.

## النطاق الحالي

- Windows 10/11 x64.
- واجهة عربية وإنجليزية.
- التكامل المستهدف: Chrome وMicrosoft Edge وFirefox؛ نشر إضافات ALHami وتسجيلها ما زال قيد الإعداد.
- مجلد بيانات ALHami مستقل عن مجلد بيانات Zajil.
- النسخة مشتقة من Zajil ومرخصة بموجب GPL-3.0-or-later. راجع [LICENSE](LICENSE) وإشعارات حقوق المؤلف.

## التطوير على Windows

المتطلبات: Rust المثبت في `rust-toolchain.toml`، وNode.js 24، وVisual Studio Build Tools مع MSVC x64 وWindows SDK.

من مجلد `apps/desktop`:

```powershell
npm ci
npm run check
npm test -- --maxWorkers=4
npm run tauri -- dev
```

لبناء تطبيق Windows محليًا:

```powershell
npm run tauri -- build
```

هذا بناء تطويري محلي. إنشاء حزمة إصدار وتوقيعها والتحديث التلقائي لم تُجهّز بعد.

## حالة العمل

يجري نقل الهوية وفصل التطبيق عن Zajil والتحقق من خط الأساس. لم تُحسم بعد هوية إضافات المتصفحات ومفاتيح تحديث ALHami وأصوله المرئية.

## الترخيص والمصدر

هذا البرنامج مشتق من [Zajil Download Manager](https://github.com/motalim-ai/zajil-download-manager)، وهو مشروع GPL-3.0-or-later. يحتفظ ALHami بإشعارات الحقوق والتراخيص المطلوبة؛ راجع [LICENSE](LICENSE) وملفات الإشعارات داخل المستودع.

---

## English

ALHami Download Manager is an open-source download manager for Windows, derived from [Zajil Download Manager](https://github.com/motalim-ai/zajil-download-manager).

**ALHami is undergoing rebranding and verification. No ALHami release or updater channel is ready yet.** Do not use Zajil releases to install or update ALHami.

The current target is Windows 10/11 x64, with Arabic and English UI. Chrome, Microsoft Edge, and Firefox integration is planned; ALHami browser add-on identities and registration are still pending. ALHami uses a separate data directory. The project is licensed under GPL-3.0-or-later; see [LICENSE](LICENSE) and the retained copyright notices.

### Windows development

Requirements: the Rust toolchain pinned in `rust-toolchain.toml`, Node.js 24, and Visual Studio Build Tools with MSVC x64 and the Windows SDK.

From `apps/desktop`:

```powershell
npm ci
npm run check
npm test -- --maxWorkers=4
npm run tauri -- dev
```

Build locally with `npm run tauri -- build`. This is a local development build; release packaging, signing, and automatic updates are not ready.
