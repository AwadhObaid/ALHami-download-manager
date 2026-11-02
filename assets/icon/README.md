# أصول علامة ALHami

- `alhami-icon.svg`: أيقونة التطبيق المتجهة، درع وسهم تنزيل.
- `alhami-mark.svg`: علامة أحادية اللون تُستخدم داخل الواجهة وفي الإضافة.
- أيقونات Windows الموزعة موجودة في `apps/desktop/src-tauri/icons/`، وتُولد من `alhami-icon.svg`:

```powershell
cd apps/desktop
npm run tauri -- icon ../../assets/icon/alhami-icon.svg --output src-tauri/icons
```

العلامة مؤقتة لمرحلة التطوير؛ لا يُنشر إصدار قبل اعتماد المالك لها.
