<div align="center">

# Catalina Correa

**Fullstack Developer** · Kotlin + Spring Boot · React + TypeScript

Buenos Aires, Argentina 🇦🇷

*Software Development Technician (UNSAM). I build client–server applications end to end:
layered architecture, REST and GraphQL APIs, hybrid persistence (SQL + NoSQL + cache),
all containerized. I'm drawn to backend work and software architecture — and lately,
to putting AI inside it.*

[![Email](https://img.shields.io/badge/Email-catalinayazmincorrea%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:catalinayazmincorrea@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Catalina_Correa-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/catalina-yazm%C3%ADn-correa-576037211)
![Spanish](https://img.shields.io/badge/Spanish-Native-555?style=for-the-badge)
![English](https://img.shields.io/badge/English-C1_Advanced-555?style=for-the-badge)

🇦🇷 [Leer en español](README.md)

</div>

---

## 🧰 Stack

| | |
|---|---|
| **Backend** | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) ![Tailwind](https://img.shields.io/badge/Tailwind_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![MUI](https://img.shields.io/badge/Material_UI-007FFF?style=flat-square&logo=mui&logoColor=white) ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white) |
| **APIs & security** | ![REST](https://img.shields.io/badge/REST-005571?style=flat-square) ![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **AI / Vision** | ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square) ![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square) ![ChromaDB](https://img.shields.io/badge/ChromaDB-FFB000?style=flat-square) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) ![YOLO](https://img.shields.io/badge/YOLO-111F68?style=flat-square) ![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square) |
| **DevOps** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white) ![Render](https://img.shields.io/badge/Render-000000?style=flat-square&logo=render&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white) ![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white) |

---

## 🚀 Featured projects

### 📚 BookLibre — book lending platform · [backend](https://github.com/CatalinaCorrea-png/booklibre-backend) · [frontend](https://github.com/CatalinaCorrea-png/booklibre-frontend)

`Kotlin` `Spring Boot` `Spring Security` `JWT` `React` `TypeScript` `Axios` `GraphQL` `PostgreSQL` `MongoDB` `Redis` `Docker`

Fullstack, team of 5, **355 backend commits**. Controller–Service–Repository layers,
a **REST + GraphQL** API (Netflix DGS), and **three data engines**: PostgreSQL through JPA,
MongoDB for the catalog, Redis as a cache.

> **My favorite part: authentication.**
>
> - **Two tokens.** The access token (an HMAC-signed JWT) carries the role and email in its *payload*
>   and travels in the `Authorization` header. The refresh token lives in an `httpOnly` +
>   `SameSite=Strict` cookie, out of JavaScript's reach, and **rotates on every use**.
> - **A custom JWT filter** in Spring Security: it tells an expired token from an invalid one, and
>   enforces role-based permissions (reader, publisher, combined) endpoint by endpoint.
> - **Single-flight refresh in Axios.** One interceptor attaches the token; the other catches the
>   401 and fires **a single refresh**: requests failing in parallel go into a *retry queue* and are
>   replayed with the new token. Without it, concurrent refreshes rotate the token out from under
>   each other and kill the session.
> - **Session handling on the frontend.** The access token lives **in memory only**. A page reload
>   restores it through a silent refresh; "remember me" picks between `localStorage` and
>   `sessionStorage`; a timer plus `visibilitychange` catch expiry even in background tabs.

**MongoDB sharding:** I compared *hash* sharding (500,024 books → **49.99% / 50%**) against *range*
sharding on `{title, bookId}` (452,000 books, pre-splitting and manual `moveChunk` → **49.83% / 50.16%**).

**Deployment:** multi-stage Dockerfile (Gradle → Temurin JRE 21), PostgreSQL on Render, MongoDB on
Atlas, configuration through environment variables. Coverage tracked with **JaCoCo**.

---

### 🚁 [AeroSearch AI](https://github.com/CatalinaCorrea-png/Proyecto-Software-2026) — drones for search and rescue

`Python` `FastAPI` `MongoDB` `YOLOv8` `OpenCV` `React 19` `TypeScript` `Leaflet` `Docker`

Drone management for search and rescue: computer vision, thermal detection, and a real-time
dashboard. **130 commits**.

- **Backend** FastAPI + MongoDB: person detection with **YOLOv8** and pose estimation over the drone's video feed.
- **Frontend** React 19 + TypeScript + Vite: maps with **Leaflet**, charts with **Recharts**.
- **Tested on both sides:** `pytest` with coverage, and `Vitest` + Testing Library + `@vitest/coverage-v8`.
- An **embedded hardware** module (PlatformIO): from firmware to dashboard.

---

### 🤖 AI Engineering — from an LLM client to an agent with memory

`LangChain` `LangGraph` `Pinecone` `ChromaDB` `Pydantic` `asyncio`

Five systems built from scratch (CoderHouse), each in its own repository:

| | What I built |
|---|---|
| **1** | An [**async, provider-agnostic LLM client**](https://github.com/CatalinaCorrea-png/pre-entrega-1-CODER-AI-ENGINEERING): OpenAI and Anthropic behind one interface — switch providers with a single config field, no rewrite needed. |
| **2** | An [**LCEL pipeline**](https://github.com/CatalinaCorrea-png/pre-entrega-2-CODER-AI-ENGINEERING) with a retry policy that **always** returns a validated Pydantic object, never raw text. |
| **3** | [**Local RAG**](https://github.com/CatalinaCorrea-png/pre-entrega-3-CODER-AI-ENGINEERING) over a persistent ChromaDB store. If the answer isn't in the documents, it says so instead of making one up. |
| **4** | [**Cloud RAG**](https://github.com/CatalinaCorrea-png/pre-entrega-4-CODER-AI-ENGINEERING): Pinecone Serverless + a **hybrid retriever** (BM25 ⊕ embeddings), **measured against a golden set** with Precision@5, Recall@5, and MRR@5. |
| **5** | A [**ReAct agent**](https://github.com/CatalinaCorrea-png/pre-entrega-5-CODER-AI-ENGINEERING) on LangGraph: a conditional edge drives the loop, not an `if/else`. **Persistent memory** in SQLite — the conversation outlives the process. |

---

### 🧊 [CLL Web](https://github.com/CatalinaCorrea-png/CLL-web) — a real client site, in production

`React` `Express` `MySQL` `Docker` `Nginx` `VPS`

Corporate site and product catalog for a commercial refrigeration company.
**It's in production and a real client depends on it.**

React + Vite; a Node/Express API on **MySQL**; Nginx on a
VPS with Docker. A **design system I built** in `theme.css`: semantic tokens and reusable utilities.

---

### 👗 Outfit Maker — [backend](https://github.com/CatalinaCorrea-png/outfit-maker-backend-kotlin) · [frontend](https://github.com/CatalinaCorrea-png/outfit-maker-frontend-react-ts)

![Status](https://img.shields.io/badge/status-in_progress-F59E0B?style=flat-square)

`Kotlin 2.3` `Spring Boot` `React 19` `Tailwind 4` `i18next`

> 🚧 Work in progress

A personal project. Kotlin + Spring Boot backend (JPA, Validation, Security + JWT);
React 19 + TypeScript frontend with Tailwind 4, **i18n through i18next**, and accessibility
(`focus-trap-react`).

---

### ☕ [Java Project — Codo a Codo](https://github.com/CatalinaCorrea-png/Proyecto-Java-CODOACODO)

`Java` `Servlets` `JDBC` `MySQL` `Jackson` `JavaScript`

A movie website in **plain Java, no frameworks**: Servlets, JDBC against MySQL, and JSON
responses through Jackson, packaged as a WAR on Tomcat. The vanilla-JavaScript frontend
consumes the TMDB API. Skipping Spring was deliberate — I wanted to understand what the
framework solves before reaching for it.

---

### 👁️ Computer vision, 100% local (personal projects)

`Python` `MediaPipe` `YOLO11` `OpenCV`

Two desktop apps, just for fun, that send nothing to any server:

- **[AirMouse](https://github.com/CatalinaCorrea-png/airmouse)** — drive the Windows mouse with your
  hand. **21 landmarks** through MediaPipe: the palm moves the cursor, thumb + index clicks and
  drags, and the middle finger grabs a window to drag it across monitors.
- **DONT-SCROLL** — **YOLO11n + MediaPipe Hands** detect when you pick up your phone while working
  and set off an alarm. A 2 s debounce and a 30 s cooldown keep it from being intrusive.

---

## 🎓 Education

| Program | Institution | Details |
|---|---|---|
| **Software Development Technician** | UNSAM | 2023 – 2026 · **18/18 courses · GPA 8.44 / 10** |
| **AI Engineering** | CoderHouse | In progress |
| **Web Application Development — Java & Spring Boot** | Talento Tech · Buenos Aires City Dept. of Education | Microcredential · Jun 2026 |
| **Fullstack React / Node / Express** | CILSA Bootcamp | 2024 |
| **Java Fullstack Programming** | Codo a Codo | 2024 |

---

## 📊 GitHub

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=CatalinaCorrea-png&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&theme=tokyonight)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=CatalinaCorrea-png&layout=compact&langs_count=8&hide_border=true&theme=tokyonight)

</div>

---

<div align="center">

**Looking for my first role as a fullstack or backend developer.**

I'm drawn to teams where architecture gets discussed and learning is taken seriously.

[![Email](https://img.shields.io/badge/Get_in_touch-catalinayazmincorrea%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:catalinayazmincorrea@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Let's_connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/catalina-yazm%C3%ADn-correa-576037211)

</div>
