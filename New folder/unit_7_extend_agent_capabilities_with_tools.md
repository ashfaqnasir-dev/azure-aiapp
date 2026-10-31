# 🛠️ Unit 7 - Extend Agent Capabilities with Tools

> **Objective:** AI agents ki taqat ko Tools (jaise Code Interpreter, File Search, Bing Search) ke zariye barhana aur unhein properly configure karna.

AI agents ka sab se bada faida yeh hai ke woh **Tools** use kar sakte hain. Tools ki madad se agent sirf text generate nahi karta, balke real-time data access, code execution, aur external systems ke sath integrate bhi kar sakta hai.

---

## 1. Understanding Agent Tools (Tool-Calling Lifecycle)

Tools woh functions ya capabilities hoti hain jinhein agent khud autonomous tareeqay se call karta hai. Yeh process **automatically** hota hai:

- [ ] **Step 1:** User agent ko message / prompt bhejta hai.
- [ ] **Step 2:** Agent analyze karta hai ke user ki request poori karne ke liye kaunsa tool chahiye.
- [ ] **Step 3:** Agent us tool ko required parameters/arguments ke sath invoke karta hai.
- [ ] **Step 4:** Tool secure sandbox ya external environment mein execute hota hai aur result wapas aata hai.
- [ ] **Step 5:** Agent us result ko naturally formulate karke response mein include karta hai.
- [ ] **Step 6:** User ko contextually accurate final response mil jata hai.

---

## 2. Built-in Tools Overview (Common Tools)

Microsoft Foundry mein tools ki 3 bunyadi categories hain:
1. **Configured** (Ready-to-use)
2. **Catalog** (Registry se add karein)
3. **Custom** (Aapke apne banaye huwe tools)

### Ahem Built-in Tools:
- [ ] **Code Interpreter:** Python code likhta aur secure isolated sandbox mein execute karta hai (Complex Math, Data Analysis, aur Visual Charts banane ke liye).
- [ ] **File Search:** RAG (Retrieval-Augmented Generation) capability ke liye. Aapki upload ki hui documents (PDF, Word, TXT, Markdown) ko vectorize aur index karke unmein se targeted answers dhoondhta hai.
- [ ] **Bing Web Search:** Real-time web data access karta hai (Current events, Breaking news, aur Trending topics ke liye).
- [ ] **Azure AI Search:** Enterprise-grade search indexes se data retrieve karta hai (File Search se kahin zyada scalable aur advanced).
- [ ] **OpenAPI Tools:** External REST APIs se connect karta hai (OpenAPI 3.0 specification schemas ke zariye).

> **Additional Tools:** Browser Automation, Computer Use, Image Generation, SharePoint, Microsoft Fabric, Deep Research, Agent-to-Agent collaboration, aur Semantic Memory.

---

## 3. Adding Tools in Visual Studio Code

VS Code mein tools add karne ke 2 ahem tareeqay hain:

### Tareeqa A: Using the Visual Designer
- [ ] Agent Designer mein apna agent open karein.
- [ ] Configuration panel mein **Tools** section mein jayein.
- [ ] **Add Tool** ya **`+`** icon par click karein.
- [ ] Library se required tool select karein aur settings configure karein.
- [ ] Changes ko save karein.

### Tareeqa B: Using YAML (Direct Edit)
Agar aap agent definition YAML file direct edit karna chahte hain, toh `tools` array mein tools ko define karein:

```yaml
version: 1.0.0
name: research-assistant
description: Helps with research tasks
model:
  id: 'gpt-4o-deployment'
instructions: |
  You're a research assistant. Use Code Interpreter for data analysis and Bing Search for current info.
tools:
  - type: code_interpreter
  - type: bing_grounding
    bing_grounding:
      connection_id: "your-connection-id"
  - type: file_search
    file_search:
      vector_store_ids:
        - "vectorstore-123"
```

> **Note:** Kuch tools ko additional parameters darkaar hote hain jaise ke `connection_id` (Bing grounding ke liye) ya `vector_store_ids` (File Search ke liye).

---

## 4. Model Context Protocol (MCP) Servers

MCP ek standardized aur open protocol hai custom tools aur data sources ko connect karne ke liye. Yeh Microsoft Foundry ke Catalog section mein milte hain.

### 3 Types of MCP Servers:
- **Remote MCP Servers:** Network / Cloud par hosted hote hain (*Production workloads ke liye best*).
- **Local MCP Servers:** Local developer machine par chalte hain (*Local debugging aur testing ke liye*).
- **Custom MCP Servers:** Aapke organization ke banaye huwe proprietary business servers.

### Major Benefits:
- **Standardized Protocol:** Universal interface across various clients.
- **Reusable Components:** Ek baar banayein, multiple agents mein reuse karein.
- **Community-driven Tools:** Pre-built connectors ka broad ecosystem.
- **Simplified Integration:** Complex custom middleware likhne ki zaroorat nahi rehti.

---

## 5. Tool Configuration Best Practices

- **Start with Built-in Tools:** Hamesha pehle out-of-the-box built-in tools use karein kyunke woh Microsoft-tested, secure, aur optimized hote hain.
- **Match Tools to Requirements:** Har tool ko clear purpose ke sath hi enable karein (har faaltu tool execution latency aur token cost barhata hai).
- **Provide Clear System Instructions:** Agent prompt mein wazeh batayein ke kaunsa tool kab aur kaise trigger karna hai (e.g., *"Use Code Interpreter strictly for mathematical calculations and regressions"*).
- **Keep Knowledge Bases Current:** File Search ya Vector Stores use karte waqt source documents ko hamesha updated aur clean rakhein.
- **Test Tool Behavior:** Azure AI Playground mein edge cases test karein ke agent theek waqt par theek function execute kar raha hai.
- **Consider Toolboxes:** Enterprise scenarios ke liye tools ko modular bundles (Toolboxes) mein rakhein taake centralized authentication, versioning, aur access governance maintain rahe.

---

## 6. Real-World Example (Multi-Tool Orchestration)

Modern agents ek single conversation mein muta'addid (multiple) tools ba-yak-waqt use kar sakte hain. Misaal ke taur par, ek **Enterprise Research Agent**:

1. **Bing Web Search** se latest market trends aur stock prices laata hai.
2. **File Search** se company ki internal Q3 financial report refer karta hai.
3. **Code Interpreter** dono data sets ko mila kar Python ke zariye comparative chart aur growth percentage calculate karta hai.

Yeh poora workflow agent autonomous plan ke mutabiq seamlessly execute karta hai.

---

## 7. Official References & Documentation

- 👉 [Microsoft Learn: Extend Agent Capabilities with Tools (Official Documentation)](https://learn.microsoft.com/azure/ai-foundry/)