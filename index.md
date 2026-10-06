---
title: ملاحظات
layout: default
---

<!--
طريقة الكتابة:
  ## اسم مجموعة      (مثلاً: Claude Code أو GitHub)  ← عنوان مجموعة في الفهرس
  ### عنوان ملاحظة                                   ← كل ملاحظة كارت لوحدها وبتظهر في الفهرس
  #### عنوان فرعي                                    ← أجزاء جوه نفس الملاحظة (مش بتظهر في الفهرس)
-->

# ملاحظاتي

## Claude Code

### ربط Hostinger بـ Claude Code (MCP)

#### لو ظهرت الرسالة دي — الاتصال محتاج تسجيل دخول تاني (مش تنصيب)

```
plugin:hostinger:hostinger: https://mcp.hostinger.com (HTTP) - ! Needs authentication
```

الحل: داخل `claude` اكتب `/mcp` ← اختار **plugin:hostinger:hostinger** ← **Authenticate** ←
انسخ الرابط في المتصفح (WSL مش بيفتح المتصفح لوحده) وتأكد إنك داخل على **الحساب الصح** قبل الموافقة.

لو السطر اختفى تمامًا من `claude mcp list` ← ساعتها بس تنصّب البلجن تاني:
`/plugin install hostinger@claude-plugins-official`

#### إضافة حساب Hostinger تاني

```bash
claude mcp add --transport http --scope user hostinger-2 https://mcp.hostinger.com
```

بعدها: افتح نافذة **خاصة (Private)** وادخل على الحساب التاني ← `/mcp` ← **hostinger-2** ← **Authenticate**.
وقت الاستخدام قول اسم الاتصال صراحة: «باستخدام hostinger-2 …».

#### التحقق

```bash
claude mcp list
```

