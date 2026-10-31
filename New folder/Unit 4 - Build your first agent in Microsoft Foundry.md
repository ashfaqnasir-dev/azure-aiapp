# 🏗️ Unit 4 - Build your first agent in Microsoft Foundry

> **Objective:** Microsoft Foundry Portal (bina coding ke) use karke apna pehla AI Agent banana, configure karna, test karna, aur deploy karna.

---

## 1. Naya Agent Kaise Banayein? (Creation Steps)
- [ ] **Step 1:** Browser mein **`https://ai.azure.com`** kholein aur apne Azure account se login karein.
- [ ] **Step 2:** Apna **Project** select karein (ya naya banayein).
- [ ] **Step 3:** Left menu mein **`Build > Agents`** par click karein.
- [ ] **Step 4:** **`Create`** (naya banane) ka button dabayein.
- [ ] **Step 5:** Ab aapse 3 cheezein maangi jayengi:
  - **Name:** Agent ka naam (jaise "Healthcare Assistant").
  - **Description:** Uska maqsad (jaise "Patient ke sawalon ke jawab dena").
  - **Model:** Dropdown se AI model select karein (jaise GPT-4o).
- [ ] **Step 6:** Bas! Aapka agent ban jayega aur uski configuration screen khul jayegi.

---

## 2. Agent Ko Sazayein (Configure Instructions)
Jab aapka agent ban jaye, toh usay kaam karna sikhana hoga.
- [ ] **Instructions:** Yahan aap batayenge ke agent ko kaise baat karni hai, kaise behave karna hai, aur kya rules follow karne hain.
- [ ] **Parameters:** Yahan aap **Temperature** (jawab kitna random ho) aur **Top P** (jawab kitna diverse ho) ko adjust kar sakte hain.

---

## 3. Agent Ko Test Karein (Playground)
Agent ko deploy (live) karne se pehle, usay test karna zaroori hai.
- [ ] Agent ke menu mein **`Playground`** tab par click karein.
- [ ] Yahan aap agent se baat cheet kar sakte hain, usay alag alag sawal pooch sakte hain, aur dekh sakte hain ke woh sahi jawab de raha hai ya nahi.

---

## 4. Agent Ke Liye Tools (Auzaar) Add Karein
Agar aap chahte hain ke aapka agent sirf baatein na kare, balke kuch kaam bhi kare (jaise files parhna ya internet search karna), toh aap Tools add kar sakte hain:
- [ ] **Configured:** Pehle se bane hue tools (jaise Code Interpreter, File Search).
- [ ] **Catalog:** Internet se add kiye jane wale tools (jaise Bing Web Search, SharePoint).
- [ ] **Custom:** Aapke khud ke banaye hue tools (OpenAPI ke zariye).

---

## 5. Agent Ko Deploy Karein
Jab aap test se khush ho jayein, toh **`Deploy`** ka button dabayein.
- [ ] Deploy hone ke baad, aap is agent ko apni app ke andar **SDK** ya **REST API** ke zariye use kar sakte hain.

---

## 💡 Exam Tip (Key Takeaways)
- **Creation:** AI Foundry portal (`ai.azure.com`) se bina code ke agent banta hai.
- **Instructions:** Agent ki shakhsiyat (personality) aur rules yahi define karte hain.
- **Playground:** Yahan agent ko test kiya jata hai.
- **Tools:** Agent ki taqat barhane ke liye (Web search, File search waghera).

---
**Status:** ✅ Unit 4 Completed