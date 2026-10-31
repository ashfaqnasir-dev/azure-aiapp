# 🎯 Unit 3 - Explore development approaches

> **Objective:** Microsoft Foundry mein AI Agent banane ke do alag alag tareeqon (Foundry Portal aur Visual Studio Code) ko samajhna aur unka comparison karna.

Yeh unit batati hai ke AI Agent banane ke liye kaunsa tareeqa (approach) kab aur kyun use karna chahiye.

---

## 1. Foundry Portal Development (Bina Coding ke)
Yeh ek Web-based interface hai (browser mein khulta hai). Ismein aapko code likhne ki zaroorat nahi hoti, bas button dabane hote hain.

**Kab use karein?**
- [ ] Jab aapko jaldi se ek idea test karna ho (Prototyping).
- [ ] Jab aap non-technical logon (jaise manager ya client) ke sath mil kar kaam karna chahte hain.
- [ ] Jab aapko saare agents ek centralized jagah se manage karne hain.

---

## 2. VS Code Development (Coding ke sath)
Agar aap ek developer hain aur code likhna pasand karte hain, to Microsoft ne **Foundry Toolkit for VS Code** banaya hai. Yeh aapke VS Code ke andar hi AI Agent banane ki taqat deta hai.

**Iske 3 Main Hissay hain:**
- [ ] **Resources:** Yahan aap apne models, agents, aur connections dekh sakte hain.
- [ ] **Tools:** Yahan Model Playground aur Agent Playground hote hain jahan aap AI ko test kar sakte hain.
- [ ] **Help & Feedback:** Documentation aur support ke liye.

**Kab use karein?**
- [ ] Jab aapko code ke sath sath agent banana ho.
- [ ] Jab aap Git (Version Control) ke zariye agent ki settings track karna chahte hain.
- [ ] Jab aapko YAML file ko direct edit karna ho.

*(Misaal: Foundry Portal factory ke manager ki tarah hai jo instructions deta hai, aur VS Code factory ke engineer ki tarah hai jo machine ke andar kaam karta hai).*

---

## 3. Typical Development Workflow (Kaam Karne Ka Tareeqa)
Chahe aap Portal use karein ya VS Code, Agent banane ka process same hai:
- [ ] **Step 1:** Project se connect karein.
- [ ] **Step 2:** Agent banayein (uska naam aur purpose batayein).
- [ ] **Step 3:** Usay Instructions dein (uska behavior set karein).
- [ ] **Step 4:** Usme Tools add karein (jaise file search ya code execution).
- [ ] **Step 5:** Playground mein test karein.
- [ ] **Step 6:** Galtiyan theek karein (Iterate karein).
- [ ] **Step 7:** Deploy karein (Production mein bhejein).
- [ ] **Step 8:** Apni app mein integrate karein.

---

## 4. Azure Resources (Kya Zaroori Hai?)
Agent banane ke liye aapko 2 main cheezein chahiye:
- [ ] **Microsoft Foundry Project:** Jahan saara data organize hota hai.
- [ ] **Model Deployments:** Jo asal AI model chalayega (jaise GPT-4).

**Optional (Agar zaroorat pare):**
- [ ] **Azure AI Search:** Agar aapko apni documents mein se data dhoondna hai.
- [ ] **Azure Storage:** Files rakhne ke liye.
- [ ] **Azure Key Vault:** Secrets (passwords) chupane ke liye.
- [ ] **Azure Functions:** Custom code chalane ke liye.

---

## 💡 Exam Tip (Key Takeaways)
- **Portal:** No Code, Quick Prototyping, aur Centralized Management ke liye best hai.
- **VS Code:** Code-first approach, Git Version Control, aur Local Development ke liye best hai.
- **Workflow:** Aksar teams dono use karti hain (Portal se demo dikhate hain, aur VS Code se asal development karte hain).

---
**Status:** ✅ Unit 3 Completed