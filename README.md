# Velos — Greek Telehealth Platform

> First Hims/Hers-style async telehealth platform for Greece. Patients submit a clinical intake form, a licensed doctor reviews within 24h, and an e-prescription is issued into the national IDIKA system — no appointment, no waiting room.

## ▶ Try the demo

1. Download **[Velos_Demo.html](./Velos_Demo.html)**
2. Open it in **Chrome or Safari**
3. No installation. No backend. No login needed.

The entire patient journey is interactive — condition selection, clinical intake questionnaire, payment simulation, prescription tracking, and a pre-loaded case history showing different statuses.

---

## What's in this repo

| File | Description |
|------|-------------|
| `Velos_Demo.html` | Standalone interactive patient app — full UI, mock API, zero dependencies |
| `README.md` | This file |

> The full backend (NestJS API, PostgreSQL schema, encryption layer, Docker setup) is in a private repository. Available on request.

---

## Product overview

Patients pick a condition → fill a 5-question clinical intake → pay → doctor reviews async → e-prescription issued to any of 11,000 Greek pharmacies via AMKA number.

**Conditions covered:** Hair loss · Erectile dysfunction · Acne & skincare · Mental health & sleep · Weight & metabolism · Women's health

---

## Tech stack

**Frontend**
- Vanilla JS single-page app — bilingual EL / EN
- Fully responsive, mobile-first

**Backend** *(private repo)*
- TypeScript · Node.js · NestJS (modular architecture)
- PostgreSQL · Prisma ORM
- AES-256 application-layer encryption for all health data
- JWT authentication (15-min access tokens + rotating refresh tokens)
- Role-based access control: Patient / Doctor / Admin
- GDPR Article 9 consent logging with timestamp + IP + user agent
- Immutable audit trail on all patient data access

**Infrastructure**
- Docker · Docker Compose (local dev — one command startup)
- AWS target: Elastic Beanstalk · RDS PostgreSQL · S3 · CloudFront
- Stripe Connect split payments · Viva Wallet · Twilio SMS · Brevo email

**Compliance**
- Greek telemedicine law (Law 5129/2024, Article 66)
- GDPR Article 9 (special category health data)
- IDIKA e-prescription system integration (national Greek platform)

---

## Key screens

| Screen | What it shows |
|--------|--------------|
| Home | Condition grid, how it works, trust signals |
| Condition detail | Treatments covered, pricing, intake preview |
| Clinical intake | Dynamic questionnaire (branches per condition), photo upload |
| Payment | Stripe / Viva Wallet / IRIS options |
| Confirmation | Case ID, prescription timeline |
| My care | Case history with status badges (New / In review / Rx ready) |
| Account | Profile, GDPR export, subscription management |

---

## Doctor dashboard

A separate authenticated app (`doctors.html`) — not included in this public demo to protect clinical logic. Shows:
- Patient case queue sorted by submission time
- Full intake answers + AI-suggested treatment hint (non-binding)
- Prescribe / Request info / Decline actions
- IDIKA e-prescription portal integration

---

## Built with AI-assisted development

This platform was designed and shipped in approximately **5 days** using Claude (Anthropic) as a pair-programming partner. I owned all product, architecture, compliance, and business decisions — Claude handled implementation. This workflow is a core part of what I bring to any product or analyst role.

---

## Contact

**Thanos Koumpanis** — Electrical & Computer Engineer, Thessaloniki, Greece

- Email: thkoumpanis@gmail.com
- LinkedIn: [linkedin.com/in/thanos-koumpanis-6097a0205](https://www.linkedin.com/in/thanos-koumpanis-6097a0205/)
