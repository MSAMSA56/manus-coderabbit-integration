# مانوس-كودر-رابيت تكامل | Manus-CodeRabbit Integration

<div dir="rtl">

## 📋 نظرة عامة

مشروع تكامل بين **Manus AI** و **CodeRabbit MCP Server** لمراجعة الكود التلقائية وتحسين جودة البرمجة.

</div>

## 🎯 Features | الميزات

- ✅ Automated code review with CodeRabbit
- 🔄 Seamless integration with Manus AI
- 🛠 Custom review rules via `.coderabbit.yaml`
- 📝 Automatic issue detection and fixing
- 🚀 CI/CD workflow automation
- 🔐 Secure environment variable management

---

<div dir="rtl">

## 📦 المتطلبات

- **Node.js** v14 أو أحدث
- **npm** (يأتي مع Node.js)
- حساب **GitHub** وتوكن الوصول (PAT)
- حساب **CodeRabbit** ومفتاح API

</div>

---

## 🚀 Installation | التثبيت

### 1. Clone the Repository

```bash
git clone https://github.com/MSAMSA56/manus-coderabbit-integration.git
cd manus-coderabbit-integration
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Copy `.env.example` to `.env` and add your credentials:

```bash
cp .env.example .env
```

Edit `.env`:

```env
GITHUB_PERSONAL_ACCESS_TOKEN=ghp_your_actual_token_here
GITHUB_PAT=ghp_your_actual_token_here
CODERABBIT_API_KEY=cr-your_actual_key_here
CODERABBIT_BASE_URL=https://api.coderabbit.ai/api/v1
CODERABBIT_LOG_LEVEL=info
```

### 4. Setup Claude Desktop (Optional)

For macOS:
```bash
# Edit: ~/Library/Application Support/Claude/claude_desktop_config.json
```

For Windows:
```bash
# Edit: %APPDATA%\Claude\claude_desktop_config.json
```

Use the configuration from `claude_desktop_config.json` file.

---

<div dir="rtl">

## 🔧 الاستخدام

### تشغيل سير العمل

```bash
node index.js
```

### سير العمل التلقائي (6 خطوات)

1. **تنفيذ الميزة**: Manus يكتب الكود
2. **إنشاء PR**: رفع Pull Request على GitHub
3. **مراجعة CodeRabbit**: تحليل الكود تلقائياً
4. **تحليل النتائج**: قراءة المشاكل المكتشفة
5. **إصلاح تلقائي**: Manus يصلح المشاكل
6. **الدمج**: دمج PR بعد الموافقة

</div>

---

## 📁 Project Structure | هيكل المشروع

```
manus-coderabbit-integration/
├── .coderabbit.yaml          # CodeRabbit custom rules
├── .env.example               # Environment variables template
├── .gitignore                 # Git ignore file
├── claude_desktop_config.json # Claude Desktop MCP configuration
├── index.js                   # Main workflow implementation
├── package.json               # Project dependencies
└── README.md                  # This file
```

---

<div dir="rtl">

## ⚙️ التكوين المتقدم

### ملف `.coderabbit.yaml`

يحتوي على قواعد المراجعة المخصصة:

- **مراجعة TypeScript**: فحص أمان الأنواع
- **مراجعة الاختبارات**: التأكد من التغطية
- **قواعد مخصصة**: منع console.log، فرض معالجة الأخطاء

### أدوات CodeRabbit MCP

```javascript
// مثال: تحليل Pull Request
await tools.analyzepullrequest({
  repository: 'owner/repo',
  pullRequestNumber: 123,
  reviewInstructions: 'Check for security and performance'
});
```

</div>

---

## 📚 Resources | المصادر

- [CodeRabbit Documentation](https://docs.coderabbit.ai)
- [GitHub API Docs](https://docs.github.com/rest)
- [Manus AI](https://manus.im)
- [MCP Protocol](https://modelcontextprotocol.io)

---

## 🤝 Contributing | المساهمة

Contributions are welcome! Please:

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

---

## 📄 License | الترخيص

MIT License - see LICENSE file for details

---

<div dir="rtl">

## 📧 التواصل

للأسئلة والدعم، يرجى فتح [Issue](https://github.com/MSAMSA56/manus-coderabbit-integration/issues)

</div>

---

<div align="center">

**Built with ❤️ by MSAMSA56**

[![GitHub](https://img.shields.io/badge/GitHub-MSAMSA56-blue)](https://github.com/MSAMSA56)

</div>
