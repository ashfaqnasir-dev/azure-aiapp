# 📝 Unit 10 - Knowledge Check (Module Assessment)

> **Objective:** Module ke concepts ko test karna aur apne answers ko future reference ke liye save karna.

---

## 1. What is the primary benefit of using Microsoft Foundry Agent Service compared to building agents with standard APIs?
- [ ] It provides access to more powerful AI models
- [ ] It requires no Azure subscription
- [x] **It handles tool calling, state management, and infrastructure automatically**
- [ ] It only works with the Azure portal

**💡 Explanation:** Standard APIs se agent banana mushkil hota hai kyunke aapko khud tools call karne hain, chat history manage karni hoti hai, aur servers ka khayal rakhna parta hai. Foundry Agent Service yeh sab (infrastructure, tool calling, state) automatically handle karta hai.

---

## 2. How does Microsoft Foundry Agent Service handle conversation state?
- [ ] By requiring developers to manually manage conversation history
- [ ] Through external database connections
- [x] **Through the Responses API which automatically manages conversation context**
- [ ] Using local file storage on the client device

**💡 Explanation:** Foundry mein **Responses API** hoti hai jo automatically user ki chat history aur context (state) ko manage karti hai, taake aapko manually database mein history save nahi karni parti.

---

## 3. Which of the following is NOT a recommended security practice for AI agents?
- [ ] Using role-based access controls
- [ ] Implementing prompt filtering and validation
- [ ] Maintaining comprehensive logging and traceability
- [x] **Allowing agents unrestricted access to all enterprise data**

**💡 Explanation:** Security ka asool hai **"Least Privilege"**. Agent ko sirf utna hi data access dena chahiye jitna uske kaam ke liye zaroori hai. Usay *unrestricted access* (sab kuch dekhne ki ijazat) dena bohot bara security risk hai.

---

## 4. What happens when an agent determines it needs a tool to respond to a user request?
- [ ] The agent asks the user for permission to use the tool
- [ ] The agent stops processing and waits for developer input
- [x] **The agent automatically invokes the tool, processes results, and incorporates them into its response**
- [ ] The agent sends the request to a separate processing queue

**💡 Explanation:** Foundry Agent Service ka sab se bada faida **Auto Tool Calling** hai. Jab agent ko lagta hai ke usay kisi tool (jaise web search ya code execution) ki zaroorat hai, to woh automatically usay call karta hai, result lata hai, aur apne jawab mein shamil kar deta hai.

---
**Status:** ✅ Knowledge Check Completed