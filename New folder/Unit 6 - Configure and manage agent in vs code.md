# ⚙️ Unit 6 - Configure and manage agent in vs code

> **Objective:** Declarative AI Agent ki settings (Instructions, Model, Temperature) ko Visual Studio Code mein configure aur manage karna.

Jab agent ban jata hai, toh asal kaam uski behaviour aur properties ko set karna hota hai. Iske liye VS Code mein 2 tareeqay hain: **Visual Agent Designer** (GUI) ya **YAML File** (Code). Dono ek dusre ke sath sync rehte hain.

---

## 1. Agent Properties (Basic Settings)
Agent Designer mein aap yeh core properties set karte hain:
- [ ] **Agent Name:** Ek descriptive naam jo agent ka maqsad bataye.
- [ ] **Model Selection:** Dropdown se apna deployed AI model (jaise GPT-4o) select karein.
- [ ] **Description:** Agent ka kaam asaan lafzon mein likhein.
- [ ] **System Instructions:** Agent ke rules aur personality define karein.
- [ ] **Agent ID:** Automatically generate hota hai (API calls ke liye use hota hai).

---

## 2. Model Configuration Options (Tuning)
AI ke jawab ko control karne ke liye yeh parameters use hote hain:
- [ ] **Temperature:** Jawab ki creativity control karta hai.
  - `0.1 - 0.3`: Focused aur consistent jawab (Business/Data tasks ke liye).
  - `0.7 - 1.0`: Creative aur random jawab.
  - `0.3 - 0.7`: Standard business agents ke liye best.
- [ ] **Top P:** Vocabulary ko limit karta hai (Default `1.0` theek rehta hai).

---

## 3. Understanding the Agent YAML Structure
Agar aap GUI ki bajaye direct code edit karna chahte hain, toh YAML file mein yeh sections hote hain:

- `version` & `name`: Basic details.
- `metadata`: Authors aur tags.
- `model`: Model ID aur parameters (Temperature, Top P).
- `instructions`: Detailed rules (pipe `|` ke zariye).
- `tools`: List of tools (khali `[]` ho sakta hai).

### 🔗 Official YAML Example Reference
Agar aapko complete YAML example dekhna hai, toh neeche diye gaye official link par click karein. Wahan aapko **"Complete YAML example"** ka code block milega jise aap direct copy kar sakte hain:

👉 **[Microsoft Learn: Configure and Manage Agents (Official Text)](https://learn.microsoft.com/en-us/training/modules/develop-ai-agents-azure-vs-code/6-configure-manage-agents?pivots=text)**

---

## 4. Benefits of YAML Configuration (Fayde)
- [ ] **Version Control:** YAML file ko Git mein track karein (rollback aur code review ke liye).
- [ ] **Bulk Updates:** Ek sath kai settings change karein.
- [ ] **Templates:** Reusable templates banayein.
- [ ] **Automation:** Scripts ke zariye configurations generate karein.
- [ ] **Real-time Validation:** VS Code syntax errors foran highlight karta hai.

---

## 5. Best Practices (Behtareen Tareeqay)
- [ ] **Version control:** YAML file ko hamesha Git mein save karein.
- [ ] **Descriptive names:** Agent ka naam aur tags clear rakhein.
- [ ] **Document instructions:** YAML mein comments add karein ke kya kyun likha.
- [ ] **Test after every change:** Har change ke baad Playground mein test karein.
- [ ] **Start simple:** Pehle basic instructions dein, phir complex karein.
- [ ] **Keep focused:** Ek agent ko bohat saare kaam na dein.

---
**Status:** ✅ Unit 6 Completed