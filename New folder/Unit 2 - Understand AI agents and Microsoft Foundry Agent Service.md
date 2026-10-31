# 🧠 Unit 2 - Understand AI agents and Microsoft Foundry Agent Service

> **Objective:** AI Agents ka asal concept, unke fayde, security risks, aur Microsoft Foundry Agent Service ki features ko samajhna.

---

## 1. AI Agent Kya Hai? (Basic Concept)
- [ ] Aam apps (jaise calculator) pehle se set rules par chalte hain. Lekin **AI Agent** ek aisa software hai jo **Generative AI** use karta hai.
- [ ] Yeh khud **context** (halaat) samajhta hai, khud **faisla** karta hai, aur goal poora karne ke liye **actions** leta hai (jaise tools ko call karna).

---

## 2. AI Agents Ke 4 Bade Fayde (Why useful?)
- [ ] **Automation:** Boring aur repeat hone wale kaam khud kar deta hai.
- [ ] **Better Decisions:** Data ko analyze karke acha faisla leta hai.
- [ ] **Scalability:** Kaam barhne par naye log hire karne ki zaroorat nahi parti.
- [ ] **24/7 Availability:** Bina thake din raat kaam karta hai.

---

## 3. AI Agents Ki Misaalein (Use Cases)
- [ ] **Personal:** Meeting schedule karna, emails likhna (jaise Microsoft 365 Copilot).
- [ ] **Research:** Market trends check karna aur reports banana.
- [ ] **Sales:** Customers ko dhoondhna aur follow-up karna.
- [ ] **Customer Service:** Customers ke sawalon ke jawab dena aur refunds process karna.
- [ ] **Developer:** Code likhna aur bug fix karna (jaise GitHub Copilot).

---

## 4. Security Risks (Sab Se Ahem Hissa)
Kyunke Agents khud se kaam karte hain, inke kuch bohot bade risks hain jinhe rokna zaroori hai:
- [ ] **Data Leakage:** Galti se koi private data customer ko na dikha de.
- [ ] **Prompt Injection:** Hacker AI ko dhoka de kar uski secret instructions chura le.
- [ ] **Unauthorized Access:** Agent ko aisi cheezon ka access mil jaye jo usay nahi milni chahiye.
- [ ] **Data Poisoning:** Hacker training data ko kharab kar de taake AI galat faisle le.
- [ ] **Supply Chain:** Agar koi teesra tool (plugin) kharab ho, to agent par asar pare.
- [ ] **Over-reliance:** AI bina permission koi galat payment ya post na kar de.
- [ ] **Inadequate Logging:** Agar AI ne kya kiya, uska record na ho.

**Hal (Mitigation):** In sab ko roknay ke liye **RBAC** (permissions), **Human-in-the-loop** (insaan ki approval), aur **Complete Logging** (record rakhna) zaroori hai.

---

## 5. Microsoft Foundry Agent Service (Yeh Kya Hai?)
- [ ] Yeh Microsoft ka ek **Fully Managed Service** hai. Iska matlab hai ke aapko servers aur storage ki tension nahi leni parti. Aap sirf **50 lines se kam code** likh kar ek AI Agent bana sakte hain.
- [ ] **Declarative Agents:** Jo code ke bajaye configuration se bante hain. (Yeh sab se aam hain).
  - [ ] *Prompt-based agents:* Single agent jo model, tools, aur instructions se banta hai.
  - [ ] *Workflow agents:* Kai agents jo aapas mein mil kar kaam karte hain (YAML mein bante hain).
- [ ] **Hosted Agents:** Jo code mein bante hain aur container ki tarah deploy hote hain.

---

## 6. Foundry Agent Service Ki Khaas Features
- [ ] **Auto Tool Calling:** Khud tools ko call karta hai, aapko lamba code nahi likhna parta.
- [ ] **Secure Data:** Conversation ki history (state) khud manage karta hai.
- [ ] **Tool Catalog:** Bohot saare ready-made tools (web search, code execution) milte hain.
- [ ] **Model Selection:** Aap apni zaroorat ke hisaab se AI model (jaise GPT-4) chun sakte hain.
- [ ] **Enterprise Security:** Data safe rakhta hai aur content filters lagata hai.
- [ ] **Observability:** Aap live dekh sakte hain ke Agent kya kar raha hai.

---

## 💡 Exam Ke Liye Nukta (Key Takeaways)
- **Service:** AI agents ko asani se banane ke liye **Microsoft Foundry Agent Service** best hai.
- **Security:** Sab se bade khatre **Prompt Injection** aur **Data Leakage** hain.

---
**Status:** ✅ Unit 2 Completed