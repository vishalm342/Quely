# Quely: Smart CRM Sales Agent - Execution Plan

## 🎯 Vision
Quely is an autonomous Sales Agent SaaS that converts natural language into complex MongoDB Aggregation queries to provide real-time business intelligence and automated outreach.

## 🛠️ Tech Stack (Track 1)
- **Framework**: Next.js 15 (App Router), Tailwind CSS
- **AI Stack**: LangChain.js, Vercel AI SDK, Gemini 1.5 Flash/Pro
- **Database**: MongoDB Atlas (Live Data + Vector Search)
- **Observability**: LangSmith

## 📁 Phase 1: Foundation (Day 1-2)
- [ ] 1.1: Initialize Next.js 15 project with TypeScript and Tailwind.
- [ ] 1.2: Set up MongoDB Atlas connection in `/src/lib/mongodb.ts`.
- [ ] 1.3: Generate and seed 50 rows of mock `customers` and `orders` data using a script.
- [ ] 1.4: Implement Clerk/NextAuth for the SaaS user layer.

## 🧠 Phase 2: The Core Agent (Day 3-4)
- [ ] 2.1: Define Zod schemas in `/src/schemas` for the database mapping.
- [ ] 2.2: Build the `NL-to-Query` tool: A function that uses Gemini to output a valid Aggregation Pipeline JSON array.
- [ ] 2.3: Create the LangChain "ReAct" Agent in `/src/agents/quelyAgent.ts` with memory retention.
- [ ] 2.4: Integrate LangSmith for tracing and debugging query logic.

## 📊 Phase 3: SaaS Interface & Actions (Day 5-6)
- [ ] 3.1: Build the Dashboard UI: A clean sidebar chat next to a dynamic data table component.
- [ ] 3.2: Implement "One-Click Outreach": A tool that takes query results and drafts personalized emails using a separate Gemini prompt.
- [ ] 3.3: Finalizing Deployment: GitHub Actions for CI/CD and hosting on Vercel.

## ⚠️ Guardrails & Rules
- All files must be small and modular (< 150 lines).
- Always use TypeScript with strict type-checking.
- Use Server Actions for all database mutations.
- If an agent task fails, provide a human-in-the-loop fallback. 