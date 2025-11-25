# 🇱🇰 Sri Lanka Bank & Branch Directory

A comprehensive, cleaned, and structured dataset of banks and their branch networks operating in **Sri Lanka**. Ideal for populating dropdowns, validating user inputs, and building fintech applications.

---

## 🚀 Features

- ⚡️ **Ready-to-use:** Provided as standard JSON.  
- 🔍 **Comprehensive:** Covers major banks (BOC, Commercial, Sampath, HNB, etc.) and finance companies.  
- 🗂 **Structured:** Organized as `Bank Name → Branch List` for easy frontend integration.  
- 🆔 **Codes Included:** Contains **Bank Codes** and **Branch Codes** for backend processing.  
- 🔤 **Sorted:** Banks and branches sorted alphabetically for better UX.

---

## 📦 Data Structure

The dataset is a single JSON object where each **key** is the bank name.

```json
{
  "Bank of Ceylon": {
    "code": "7010",
    "branches": [
      { "name": "City Office", "code": "1" },
      { "name": "Galle Fort", "code": "3" },
      { "name": "Kandy", "code": "2" }
      // ... more branches
    ]
  },
  "Sampath Bank PLC": {
    "code": "7278",
    "branches": [
      { "name": "Head Office", "code": "1" }
      // ... more branches
    ]
  }
}
```

---

## 💻 Usage

### JavaScript / React / Node.js

```js
import bankData from "./bank_data.json";

// Get list of Bank Names for a dropdown
const bankNames = Object.keys(bankData);

// Get branches for a specific bank
const getBranches = (bankName) => {
  return bankData[bankName]?.branches || [];
};

console.log(getBranches("Bank of Ceylon"));
// → [{ name: "City Office", code: "1" }, ...]
```

### Python

```python
import json

with open("bank_data.json", "r", encoding="utf-8") as f:
    data = json.load(f)

# Print code for Commercial Bank
print(data["Commercial Bank Of Ceylon PLC"]["code"])
```

---

## 🛠 Generation Script

If you have the raw CSV source files and need to regenerate the JSON, use the included Python script.

1. Place the source CSV files in the repository root:
   - `LPPL_BankBranchDirectory_AllProducts_20251114 - Bank.csv`
   - `LPPL_BankBranchDirectory_AllProducts_20251114 - Branch NEW.csv`
2. Run the generator:
   ```bash
   python generate_json.py
   ```

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<p align="center">Made by ChocoJaYY with ❤️ for the 🇱🇰 Developer Community</p>
