<div align="center">

# LUFT

**Volleyball tournament and league platform, live in production with a real community.**

[![Live](https://img.shields.io/badge/Live-luft--vb.com-0d1117?style=for-the-badge&logo=vercel&logoColor=white)](https://luft-vb.com)
![Own product](https://img.shields.io/badge/Own%20product-built%20solo-0d1117?style=for-the-badge)

![LUFT on desktop and mobile](screenshots/cover.png)

</div>

> This is a showcase repo. LUFT's source code is private, so this page covers what it does, how it's built and what it looks like. Happy to walk through the code on a call.

## The problem

Local volleyball leagues were running tournaments and drop-in sessions through spreadsheets and group chats. Bracket seeding, live scoring, roster splitting and payment tracking were slow, error-prone and confusing for organisers, referees and players alike.

## What I built

LUFT is my own product. I designed, built and run it solo, end to end.

- **Drag-and-drop bracket seeding** so organisers set up tournaments in minutes
- **Group standings** with proper tiebreaker logic
- **Live match scoreboard** that referees score courtside, with real-time push notifications to players
- **Session and roster splitting** for pickup play
- **Player training and progress tracking**
- **Multi-role authentication** for organisers, court managers, referees and players, each with their own views
- **Media uploads** for photos from game days
- **Fully custom UI**, built without a component library, mobile-first for courtside use

## Screenshots

<div align="center">
<img src="screenshots/mobile-1.png" width="23%" />
<img src="screenshots/mobile-2.png" width="23%" />
<img src="screenshots/mobile-3.png" width="23%" />
<img src="screenshots/mobile-4.png" width="23%" />
</div>

## Architecture

```mermaid
flowchart LR
    P[Players, referees<br/>and organisers] --> W[Next.js 16 app<br/>React 19 + TypeScript]
    W --> DB[(Supabase<br/>Postgres + Auth)]
    W --> R2[Cloudflare R2<br/>media storage]
    W --> T[Cloudflare Turnstile<br/>bot protection]
    W --> E[Resend<br/>transactional email]
    W --> WP[Web Push<br/>live score alerts]
    V[Vercel] -. hosts .-> W
```

## Tech stack

![Next.js](https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_R2-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Resend](https://img.shields.io/badge/Resend-000000?style=flat-square&logo=resend&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

dnd-kit for drag and drop, Web Push for notifications.

## Contact

**Muhammad Izhar** · [izhar.dev](https://izhar.dev) · [LinkedIn](https://linkedin.com/in/izharrr99) · muhammad.izhar11@gmail.com
