<div align="center">

# Catalina Correa

**Fullstack Developer** · Kotlin + Spring Boot · React + TypeScript

Buenos Aires, Argentina 🇦🇷

*Técnica en Programación Informática (UNSAM). Construyo aplicaciones cliente-servidor
de punta a punta: arquitectura en capas, APIs REST y GraphQL, persistencia híbrida
(SQL + NoSQL + caché) y todo containerizado. Me interesa el backend y la arquitectura
de software — y últimamente, meterle IA adentro.*

[![Email](https://img.shields.io/badge/Email-catalinayazmincorrea%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:catalinayazmincorrea@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Catalina_Correa-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/catalina-yazm%C3%ADn-correa-576037211)
![Español](https://img.shields.io/badge/Español-Nativo-555?style=for-the-badge)
![English](https://img.shields.io/badge/English-C1_Advanced-555?style=for-the-badge)

🇬🇧 [Read this in English](README.en.md)

</div>

---

## 🧰 Stack

| | |
|---|---|
| **Backend** | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) ![Tailwind](https://img.shields.io/badge/Tailwind_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![MUI](https://img.shields.io/badge/Material_UI-007FFF?style=flat-square&logo=mui&logoColor=white) ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white) |
| **APIs y seguridad** | ![REST](https://img.shields.io/badge/REST-005571?style=flat-square) ![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white) |
| **Datos** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **IA / Visión** | ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square) ![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square) ![ChromaDB](https://img.shields.io/badge/ChromaDB-FFB000?style=flat-square) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) ![YOLO](https://img.shields.io/badge/YOLO-111F68?style=flat-square) ![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square) |
| **DevOps** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white) ![Render](https://img.shields.io/badge/Render-000000?style=flat-square&logo=render&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white) ![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white) |

---

## 🚀 Proyectos destacados

### 📚 BookLibre — Plataforma de préstamo de libros · [backend](https://github.com/CatalinaCorrea-png/booklibre-backend) · [frontend](https://github.com/CatalinaCorrea-png/booklibre-frontend)

`Kotlin` `Spring Boot` `Spring Security` `JWT` `React` `TypeScript` `Axios` `GraphQL` `PostgreSQL` `MongoDB` `Redis` `Docker`

Fullstack, equipo de 5, **355 commits** en el backend. Capas Controller–Service–Repository,
API **REST + GraphQL** (Netflix DGS) y **tres motores de datos**: PostgreSQL vía JPA,
MongoDB para el catálogo, Redis como caché.

> **Lo que más me gustó: la autenticación.**
>
> - **Dos tokens.** El access token (JWT firmado con HMAC) lleva el rol y el email en el *payload* y
>   viaja en el header `Authorization`. El refresh token va en una cookie `httpOnly` +
>   `SameSite=Strict`, fuera del alcance de JavaScript, y **rota en cada uso**.
> - **Filtro JWT propio** en Spring Security: distingue un token vencido de uno inválido, y aplica
>   permisos por rol (lector, publicador, combinado) endpoint por endpoint.
> - **Refresh *single-flight* en Axios.** Un interceptor adjunta el token; el otro atrapa el 401 y
>   dispara **un solo refresh**: las requests que fallan en paralelo van a una *retry queue* y se
>   reintentan con el token nuevo. Sin eso, los refreshes concurrentes se rotan el token entre sí
>   y cierran la sesión.
> - **Sesión en el front.** El access token vive **solo en memoria**. Al recargar la página se
>   recupera con un refresh silencioso; "recordarme" elige entre `localStorage` y `sessionStorage`;
>   un timer más `visibilitychange` detectan el vencimiento incluso en pestañas en segundo plano.

**Sharding en MongoDB:** comparé *hash* (500.024 libros → **49,99 % / 50 %**) contra *rango* sobre
`{title, bookId}` (452.000 libros, pre-split y `moveChunk` manual → **49,83 % / 50,16 %**).

**Deploy:** Dockerfile multi-stage (Gradle → Temurin JRE 21), PostgreSQL en Render, MongoDB en Atlas,
configuración por variables de entorno. Cobertura con **JaCoCo**.

---

### 🚁 [AeroSearch AI](https://github.com/CatalinaCorrea-png/Proyecto-Software-2026) — drones para búsqueda y rescate

`Python` `FastAPI` `MongoDB` `YOLOv8` `OpenCV` `React 19` `TypeScript` `Leaflet` `Docker`

Gestión de drones para búsqueda y rescate: visión por computadora, detección térmica y
dashboard en tiempo real. **130 commits**.

- **Backend** FastAPI + MongoDB: detección de personas con **YOLOv8** y estimación de pose sobre el video del dron.
- **Frontend** React 19 + TypeScript + Vite: mapas con **Leaflet**, gráficos con **Recharts**.
- **Tests de los dos lados:** `pytest` con cobertura, y `Vitest` + Testing Library + `@vitest/coverage-v8`.
- Módulo de **hardware embebido** (PlatformIO): del firmware al dashboard.

---

### 🤖 AI Engineering — de un cliente de LLM a un agente con memoria

`LangChain` `LangGraph` `Pinecone` `ChromaDB` `Pydantic` `asyncio`

Cinco sistemas construidos desde cero (CoderHouse), cada uno en su repo:

| | Qué construí |
|---|---|
| **1** | [Cliente de LLM **asíncrono y agnóstico al proveedor**](https://github.com/CatalinaCorrea-png/pre-entrega-1-CODER-AI-ENGINEERING): OpenAI y Anthropic tras una sola interfaz — cambio de proveedor con un campo de configuración, sin reescribir código. |
| **2** | [Pipeline **LCEL**](https://github.com/CatalinaCorrea-png/pre-entrega-2-CODER-AI-ENGINEERING) con política de reintentos que devuelve **siempre** un objeto Pydantic validado, nunca texto crudo. |
| **3** | [**RAG local**](https://github.com/CatalinaCorrea-png/pre-entrega-3-CODER-AI-ENGINEERING) sobre ChromaDB persistente. Si la respuesta no está en los documentos, lo dice en lugar de inventar. |
| **4** | [**RAG en la nube**](https://github.com/CatalinaCorrea-png/pre-entrega-4-CODER-AI-ENGINEERING): Pinecone Serverless + **retriever híbrido** (BM25 ⊕ embeddings), **medido contra un golden set** con Precision@5, Recall@5 y MRR@5. |
| **5** | [**Agente ReAct**](https://github.com/CatalinaCorrea-png/pre-entrega-5-CODER-AI-ENGINEERING) con LangGraph: el ciclo lo dirige una arista condicional, no un `if/else`. **Memoria persistente** en SQLite — la conversación sobrevive al proceso. |

---

### 🧊 [CLL Web](https://github.com/CatalinaCorrea-png/CLL-web) — sitio de un cliente real, en producción

`React` `Express` `MySQL` `Docker` `Nginx` `VPS`

Sitio institucional y catálogo para una empresa de refrigeración comercial.
**Está en producción y lo usa un cliente.**

React + Vite; API Node/Express sobre **MySQL**; Nginx sobre
un VPS con Docker. **Sistema de diseño propio** en `theme.css`: tokens semánticos y utilidades
reutilizables.

---

### 👗 Outfit Maker — [backend](https://github.com/CatalinaCorrea-png/outfit-maker-backend-kotlin) · [frontend](https://github.com/CatalinaCorrea-png/outfit-maker-frontend-react-ts)

![Estado](https://img.shields.io/badge/estado-en_desarrollo-F59E0B?style=flat-square)

`Kotlin 2.3` `Spring Boot` `React 19` `Tailwind 4` `i18next`

> 🚧 Proyecto en curso

Proyecto propio. Backend Kotlin + Spring Boot (JPA, Validation, Security + JWT);
frontend React 19 + TypeScript con Tailwind 4, **i18n con i18next** y accesibilidad
(`focus-trap-react`).

---

### ☕ [Proyecto Java — Codo a Codo](https://github.com/CatalinaCorrea-png/Proyecto-Java-CODOACODO)

`Java` `Servlets` `JDBC` `MySQL` `Jackson` `JavaScript`

Web de películas con **Java puro, sin frameworks**: Servlets, JDBC contra MySQL y respuestas
JSON con Jackson, empaquetado como WAR sobre Tomcat. El frontend en JavaScript vanilla
consume la API de TMDB. Hacerlo sin Spring fue a propósito: entender qué resuelve el
framework antes de usarlo.

---

### 👁️ Visión por computadora, 100% local (proyectos propios)

`Python` `MediaPipe` `YOLO11` `OpenCV`

Dos apps de escritorio, para jugar, que no mandan nada a ningún servidor:

- **[AirMouse](https://github.com/CatalinaCorrea-png/airmouse)** — manejás el mouse de Windows con
  la mano. **21 landmarks** con MediaPipe: la palma mueve el cursor, pulgar + índice hace click y
  drag, y el dedo mayor agarra una ventana para arrastrarla entre monitores.
- **DONT-SCROLL** — **YOLO11n + MediaPipe Hands** detectan cuándo agarrás el celular mientras
  trabajás y te tira una alarma. *Debounce* de 2 s y *cooldown* de 30 s para no ser invasivo.

---

## 🎓 Formación

| Formación | Institución | Detalle |
|---|---|---|
| **Técnica en Programación Informática** | UNSAM | 2023 – 2026 · **18/18 materias · promedio 8,44** |
| **AI Engineering** | CoderHouse | En curso |
| **Desarrollo de Aplicaciones Web — Java & Spring Boot** | Talento Tech · Min. de Educación CABA | Microcredencial · jun. 2026 |
| **Fullstack React / Node / Express** | Bootcamp CILSA | 2024 |
| **Programación Java Fullstack** | Codo a Codo | 2024 |

---

## 📊 GitHub

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=CatalinaCorrea-png&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&theme=tokyonight)
![Lenguajes](https://github-readme-stats.vercel.app/api/top-langs/?username=CatalinaCorrea-png&layout=compact&langs_count=8&hide_border=true&theme=tokyonight)

</div>

---

<div align="center">

**Buscando mi primer rol como desarrolladora fullstack o backend.**

Me interesan los equipos donde se discuta arquitectura y se aprenda en serio.

[![Email](https://img.shields.io/badge/Escribime-catalinayazmincorrea%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:catalinayazmincorrea@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectemos-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/catalina-yazm%C3%ADn-correa-576037211)

</div>
