<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b0d10,100:8faecf&height=200&section=header&text=Melih%20Ilker&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Full%20Stack%20Developer%20%C2%B7%20Istanbul&descSize=18&descAlignY=58" alt="Melih Ilker, Full Stack Developer in Istanbul" width="100%" />
</p>

<p align="center">
  <a href="https://melihilker-portfolio.vercel.app">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1400&color=8FAECF&center=true&vCenter=true&width=640&lines=TypeScript+%C2%B7+React+%C2%B7+Next.js+%C2%B7+Node.js+%C2%B7+PostgreSQL;Who+can+read+which+row%3F+That's+my+favourite+question.;Sessions+that+die+when+they+should.;Open+to+Junior+Full+Stack+roles+%E2%9C%A6+Istanbul+or+remote" alt="TypeScript, React, Next.js, Node.js, PostgreSQL. Open to Junior Full Stack roles." />
  </a>
</p>

<p align="center">
  <a href="https://melihilker.vercel.app"><img src="https://img.shields.io/badge/Portfolio-0b0d10?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="https://linkedin.com/in/melihilker"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:melihilker9@gmail.com"><img src="https://img.shields.io/badge/Email-8faecf?style=for-the-badge&logo=gmail&logoColor=0b0d10" alt="Email" /></a>
  <a href="https://melihilker.vercel.app/Melih_Ilker_CV.pdf"><img src="https://img.shields.io/badge/CV-PDF-2d333b?style=for-the-badge&logo=readdotcv&logoColor=white" alt="CV" /></a>
</p>

---

### 👋 Hey there

I build web applications end to end, from the database schema to the last pixel, and I've been doing it for clients since **2021**.
What I enjoy most is the part users never see: **who is allowed to read which row**, how a session dies when it should,
and what happens when someone sends the same request 500 times.

> 🟢 **Open to Junior Full Stack · backend (Node.js) · frontend (React) roles, in Istanbul or remote.**

---

### 🚀 Selected work

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://sporliyo.com">⚽ Sporliyo</a></h3>
      <img src="https://img.shields.io/badge/status-live-2ea043?style=flat-square" alt="live" />
      <img src="https://img.shields.io/badge/role-co--developer-8faecf?style=flat-square" alt="co-developer" />
      <p>SaaS for football academies. Admins, coaches and parents each get their own dashboard for students, groups, training sessions, attendance, dues and CSV reports. Data is filtered on the server by role, so each user only loads what their role is allowed to see.</p>
      <sub><b>Next.js 16 · React 19 · Neon Postgres · Zod · Vercel Blob</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/MelihIlker/Solopreneur">🔐 Solopreneur</a></h3>
      <img src="https://img.shields.io/badge/status-open%20source-8faecf?style=flat-square" alt="open source" />
      <img src="https://img.shields.io/badge/focus-security-d29922?style=flat-square" alt="security" />
      <p>Client and project management, built security-first. It uses Redis-backed sessions instead of stateless JWT (revoking one takes effect instantly on every device), Postgres RLS with default deny, Argon2 hashing, and CI on GitHub Actions.</p>
      <sub><b>Express · Next.js · Supabase · Redis · Docker Compose</b></sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🎮 NullSect Development</h3>
      <img src="https://img.shields.io/badge/status-commercial-a371f7?style=flat-square" alt="commercial" />
      <img src="https://img.shields.io/badge/first%20month-14%20sales-2ea043?style=flat-square" alt="14 sales in the first month" />
      <p>Multiplayer game-server plugins that a partner and I build end to end, from Lua server logic to React + TypeScript interfaces and MySQL persistence.</p>
      <sub><b>Lua · React · TypeScript · MySQL</b></sub>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/MelihIlker/portfolio">🌐 Portfolio</a></h3>
      <img src="https://img.shields.io/badge/status-live-2ea043?style=flat-square" alt="live" />
      <img src="https://img.shields.io/badge/i18n-EN%20%2F%20TR-8faecf?style=flat-square" alt="EN / TR" />
      <p>A bilingual personal site, prerendered to static HTML with a custom SSR script. It has its own URL per language, generated SEO (Open Graph, JSON-LD, sitemap) and full reduced-motion support.</p>
      <sub><b>React 19 · TypeScript · Tailwind CSS v4 · Vite</b></sub>
    </td>
  </tr>
</table>

<details>
  <summary><b>🔍 Peek inside: how a request moves through Solopreneur</b></summary>
  <br>

```mermaid
flowchart LR
    U(["Browser"]) -->|"HTTP-only cookie"| N["Next.js frontend"]
    N -->|"REST"| A["Express API"]
    A --> RL{"Rate limit (Redis INCR)"}
    RL -->|"too many"| X["429 Too Many Requests"]
    RL -->|"ok"| S{"Session valid?"}
    S -->|"lookup"| R[("Redis sessions")]
    S -->|"no"| D["401 Unauthorized"]
    S -->|"yes"| SV["Service layer: Zod + authorization"]
    SV --> RP["Repository layer"]
    RP -->|"RLS default deny"| P[("Postgres")]
```

<sub>The frontend never talks to the database. Every row is protected by Row Level Security, and every session can be killed server-side.</sub>

---

### 🧰 Tech I work with

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,react,nextjs,nodejs,express,tailwind,vite&theme=dark" alt="TypeScript, JavaScript, React, Next.js, Node.js, Express, Tailwind CSS, Vite" /><br>
  <img src="https://skillicons.dev/icons?i=postgres,mysql,redis,supabase,docker,aws,git,githubactions&theme=dark" alt="PostgreSQL, MySQL, Redis, Supabase, Docker, AWS, Git, GitHub Actions" /><br>
  <img src="https://skillicons.dev/icons?i=cs,dotnet,lua&theme=dark" alt="C#, .NET, Lua" />
</p>

---

<details>
  <summary><b>📜 Experience timeline</b></summary>
  <br>

| When | What | Highlights |
|---|---|---|
| **2021 → now** | Freelance full stack developer | Client web apps end to end · REST APIs with JWT, RBAC, Redis rate limiting · Amazon S3 (presigned URLs, IAM) |
| **Oct 2025 → Mar 2026** | WestLA Online | Community platform with real-time notifications and an admin panel · reached **100+ daily active users** |
| **Sep 2023 → Jun 2024** | Panasonic Electric Works Turkey | Full stack software developer intern · C# / ASP.NET MVC admin panel · real-time IT dashboard |
| **2025 → 2027** | Bandırma Onyedi Eylül University | Associate degree, Computer Programming |

</details>

<details>
  <summary><b>🛡️ Things I care about when I build</b></summary>
  <br>

- **Access control first.** RBAC and row-level rules are designed before the first endpoint.
- **Revocable sessions.** If a session can't be killed from the server, it isn't really under control.
- **Validate at the edge.** Every input goes through a schema (Zod) before it reaches business logic.
- **Boring, typed code.** TypeScript end to end, clear layers, nothing clever that the next person has to decode.

</details>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:8faecf,100:0b0d10&height=110&section=footer" alt="" width="100%" />
</p>
