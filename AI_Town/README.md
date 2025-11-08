# 🧠 AI Town – Multi-Agent Simulation System

**Type:** Independent System Design & Research  
**Timeline:** 09/2025 
**Tech Stack:** Python · Django · Phaser · JSON Event Logs  

---

## 🎯 Overview

**AI Town** explores how an information system can model autonomous decision-making, memory, and communication.  
Inspired by **Stanford’s Generative Agents**, this project implements a small virtual town where each NPC is an intelligent agent operating through a continuous loop of:

> **Perception → Memory → Reflection → Decision → Communication**

The project aligns with my **Information Systems / Information Management** focus:  
a system’s true value lies in how effectively it structures, preserves, and routes information to generate transparent, explainable behaviors.

---

## 🧩 Goals & Outcomes

- Developed a **lightweight multi-agent framework** with configurable agents and simulation ticks.  
- Implemented **short-term and long-term memory** with reflective feedback loops for adaptive planning.  
- Designed a **JSON-based message protocol and event log** for reproducible state tracking (timestamp, sender, receiver, intent, outcome).  
- Built a **browser-based visual dashboard (Phaser)** for observing movement, dialogue, and social dynamics in real time.  
- Generated **structured logs** enabling downstream analysis of cooperation, diffusion, and behavioral patterns — ensuring traceability and auditability.

---

## 🧠 Why It Fits Information Systems / Management

- **Information Architecture:** Well-defined schemas for agent state, goals, and inter-agent communication.  
- **Data Governance by Design:** Deterministic event lineage — who did what, when, and under what context.  
- **Decision Support:** Internal logs form a dynamic knowledge base, turning behavioral data into actionable insights.

---

## 💼 My Role & Contributions

- **System & Data Modeling** – Defined entities for memory, goals, and observations; normalized JSON records for replayability.  
- **Behavior Engine** – Combined rule-based logic with reflective learning (e.g., repeated failures lower an action’s utility).  
- **Communication Protocol** – Designed structured message envelopes and delivery modes (broadcast, direct, group).  
- **Visualization** – Integrated Django backend with Phaser dashboard for real-time monitoring.  
- **Analytics Pipeline** – Logged all actions and states to structured datasets for sequence analysis and KPI inspection.

---

## 🏗️ System Architecture

| **Layer**         | **Purpose**                             | **Example**                                   |
| :---------------- | :-------------------------------------- | :-------------------------------------------- |
| **Perception**    | Collect environment data                | Detects time change → updates routine         |
| **Memory**        | Store summarized experiences            | “Met Alice at Café 10:00” tagged as ‘social’  |
| **Reflection**    | Reevaluate past outcomes                | Recalls failure → increases “practice” weight |
| **Decision**      | Choose next action via priority/utility | Selects “work” > “chat” > “wander”            |
| **Communication** | Exchange structured messages            | Broadcast “Need help with task X”             |

**Data Lineage:**  
Every message or action emits a timestamped log with actor, state, and result for full reproducibility.

---

## 🧪 Example Scenarios

- **Routine Formation:** Agents learn punctuality after repeated failures.  
- **Information Diffusion:** A broadcast spreads through social ties; reflection alters forwarding decisions.  
- **Conflict & Recovery:** Negative outcomes are logged and lower risky behavior probabilities temporarily.

---

## 💡 Insights

This project reframes an information system as a **living network of feedback and memory** rather than a static database.  
By emphasizing **traceability**, **structure**, and **iteration**, I found that the same governance principles keeping enterprise data reliable also make agent behavior explainable.

> “An intelligent system is not defined by how much data it has, but by how well it remembers and learns from its own history.”

---

## 🧩 Skills Demonstrated

Multi-Agent Systems · Information Architecture · Data Governance & Lineage · Behavioral Modeling · Front-end Visualization · Analytical Logging  

---

## 💬 Note

All data, dialogues, and scenarios were created for demonstration purposes.  
No proprietary or confidential materials were used.