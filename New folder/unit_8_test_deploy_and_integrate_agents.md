# 🚀 Unit 8 - Test, deploy, and integrate agents

> **Objective:** AI Agent ko test karna, Foundry project par deploy karna, aur external applications (jaise Teams, Copilot) ke liye publish karna.

---

## 1. Testing Strategies for Agents (Agent Ko Test Karna)

Deploy karne se pehle agent ko portal ya VS Code ke **Playground** mein test karna zaroori hai:

- [ ] **Happy Path Testing:** Common aur expected requests check karein.
- [ ] **Edge Case Testing:** Adhoori ya ajeeb requests dein taake pata chale agent uncertainty ko kaise handle karta hai.
- [ ] **Boundary Testing:** Out-of-scope requests test karein taake pata chale agent apni limits mein rehta hai ya nahi.
- [ ] **Multi-turn Conversation:** Lambi baat cheet karke check karein ke agent context yaad rakhta hai.
- [ ] **Tool Invocation:** Check karein ke agent sahi waqt par sahi tool call kar raha hai.
- [ ] **Record Results:** Test results save karein taake future mein improvements track ho sakein.

---

## 2. Deploying Agents to Your Project (Deploy Karna)

Deploy karne ka matlab hai agent ki configuration ko Foundry project mein save karna taake aap usay test aur iterate kar sakein.

### Deploying from Foundry Portal
- [ ] Foundry portal mein apne agent ke paas jayein.
- [ ] Configuration aur test results verify karein.
- [ ] **Save** par click karein aur deployment settings confirm karein.

### Deploying from Visual Studio Code
- [ ] Foundry Toolkit mein agent kholein.
- [ ] **Save to Foundry** par click karein.
- [ ] **Hosted Agents ke liye:** `+Build` menu se **Deploy to Microsoft Foundry** select karein.
- [ ] Deployment method chunein: **ZIP Code** (bina container ke) ya **Container (BYOI)** (pre-built image se).
- [ ] Model select karein aur confirm karein.

---

## 3. Publishing Agents to an Endpoint (Publish Karna)

Jab agent Foundry mein banta hai, toh usay automatically 3 cheezein milti hain:

- [ ] **Stable Endpoint:** Ek permanent URL jo versions update hone par bhi change nahi hota.
- [ ] **Entra Agent Identity:** Agent ka apna alag Microsoft Entra ID (RBAC scope).
- [ ] **Authentication Policy:** Built-in Entra ID authentication. *(API key support nahi hai).*

> **⚠️ Ahem Baat:** Agent ki apni identity hoti hai. Agar aap agent ko kisi resource ka access dena chahte hain, toh aapko us **Agent Identity** ko alag se RBAC role assign karna hoga. Warna deploy hone ke baad tools authorization errors denge.

---

## 4. Publishing to Teams & Microsoft 365 Copilot

- [ ] Foundry portal se **Microsoft Teams** aur **Microsoft 365 Copilot** par ek hi click mein publish kar sakte hain.
- [ ] Users wahan se directly agent ko use kar sakte hain.

---

## 5. The Agent Endpoint (Agent Ka URL)

Agent **Responses API protocol** use karta hai. URL format:

```text
https://<resource-name>.services.ai.azure.com/api/projects/<project-name>/agents/<agent-name>/endpoint/protocols/openai/responses
```

### Verifying the Endpoint (Test Karna)
- [ ] **Step 1:** Azure CLI se token lein:
  ```bash
  az account get-access-token --resource https://ai.azure.com
  ```
- [ ] **Step 2:** `curl` command se POST request bhejein (Authorization header ke sath).
- [ ] **Note:** Agar `403 Forbidden` error aaye, toh caller identity ko **Foundry User** role assign karein.

---

## 6. Updating Agents (Agent Update Karna)

- [ ] Development environment mein changes karein aur test karein.
- [ ] Foundry portal mein updated configuration save karein.
- [ ] Endpoint automatically naye version par traffic route kar dega (URL change nahi hoga).

---

## 7. Generating Integration Code (Code Generate Karna)

- [ ] VS Code ke Foundry Toolkit mein deployed agent select karein.
- [ ] **View Code** par click karein.
- [ ] Extension automatically boilerplate integration code generate kar dega (Authentication, Connection, Messaging, aur Response processing ke liye).

### Common Integration Patterns
- [ ] **Web Applications:** User messages Responses API par bhejein aur UI mein display karein.
- [ ] **API-driven Workflows:** Backend services se agent ko programmatically call karein.
- [ ] **Chatbot Interfaces:** User sessions ko stateful conversations se map karein.
- [ ] **Background Automation:** Scheduled tasks aur cron jobs ke liye agent calls configure karein.

---

## 8. Production Considerations (Production Ke Liye Zaroori Baatein)

- [ ] **Monitoring:** Application Insights se latency / response times, failure rates, aur token consumption track karein.
- [ ] **Security:** Managed Identities aur least-privilege RBAC policies follow karein.
- [ ] **Cost Management:** Token consumption pattern monitor karein aur rate limits / quotas set karein.
- [ ] **Error Handling:** Transient network errors ke liye exponential backoff retry logic lagayein.
- [ ] **Conversation Management:** Agent endpoints stateless model follow karte hain, is liye client application ko chat history manage karni hogi agar session continuity darkaar ho.

---

**Status:** ✅ Unit 8 Completed