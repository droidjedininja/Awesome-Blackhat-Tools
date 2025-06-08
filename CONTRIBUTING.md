# 🧩 Contributing to Awesome Black Hat Tools

Welcome! This project is a community-maintained archive of cutting-edge tools presented at **Black Hat Arsenal** events. We’re excited to have you contribute and help make this the go-to collection for red teamers, blue teamers, reverse engineers, and security researchers.

---

## 📁 Repository Structure

```bash
Awesome-BlackHat-Tools/
├── tools/
│   ├── regions/
│   │   ├── USA/
│   │   │   └── 2024/
│   │   │       └── toolname.json
│   │   └── Europe/
│   │       └── 2024/
│   │           └── toolname.json
│   └── categories/
│       ├── Red Teaming/
│       │   └── 2024/
│       │       └── toolname.json
│       └── Malware Analysis/
│           └── 2023/
│               └── toolname.json
````
### Organization

- Tools are grouped in two views:
  - **By region** under `tools/regions/`
  - **By category/track** under `tools/categories/`
- Each tool lives inside the **corresponding year folder** as a `.json` file

---

## 🧠 Tool JSON Format

Each tool must be submitted as a `.json` file with the following structure:

```json
{
  "Tool Name": "Cool Exploit Framework",
  "Description": "A modular post-exploitation tool for cloud environments.",
  "Github URL": "https://github.com/username/tool",
  "Tracks": ["Track: Exploit Development"],
  "Speakers": ["Jane Doe"],
  "Source Event": "Black Hat USA",
  "Year": 2024
}
```

### ✅ Required Fields:

- `Tool Name`: The name of the tool  
- `Description`: 1–3 concise technical sentences  
- `Github URL`: Public repository or homepage (if available)  
- `Tracks`: One or more from the approved list below  
- `Speakers`: Presenter(s) or authors of the tool  
- `Source Event`: Example: `"Black Hat Europe"`  
- `Year`: The event year

---

## 🧭 Approved Track Names

Use one or more of these exact track names:

- Track: Red Teaming  
- Track: Blue Teaming  
- Track: OSINT & Recon  
- Track: Exploit Development  
- Track: Malware Analysis  
- Track: DFIR & Forensics  
- Track: Threat Intelligence  
- Track: ICS/IoT/SCADA  
- Track: Application Security (AppSec)

> 🔹 If your tool doesn’t fit any of these, you may omit the `Tracks` field and it will be classified as `Uncategorized`.

---

## 🧪 Validation Checklist

Before submitting:

- ✅ Validate your `.json` file using a JSON linter  
- ✅ Ensure correct folder structure and filename  
- ✅ Add the file to **both** `tools/regions/{LOCATION}/{YEAR}/` and `tools/categories/{TRACK}/{YEAR}/` if applicable  
- ✅ Avoid excessive marketing or vague descriptions  

---

## 🔁 Pull Request Guidelines

- 📦 One PR per tool or logically grouped tools  
- 📌 Title format: `Add Tool: ToolName (Europe 2024)`  
- 📂 Place your files correctly – we’ll take care of generating README entries

---

## ❓ Need Help?

If you’re unsure about where to place a tool or how to format a field, don’t worry! Open an issue or leave a comment on your pull request — we’re happy to assist.

---

Thanks for contributing to **Awesome Black Hat Tools** and helping the cybersecurity community discover amazing new tools! 💻🛡️
