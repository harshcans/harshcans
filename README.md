<!--
  PROFILE README for github.com/harshcans

  SETUP
  1. Create a PUBLIC repository named exactly: harshcans   (github.com/harshcans/harshcans)
  2. Add this file as README.md and commit it to the main branch.
  3. Search this file for "EDIT" and replace those few values, then delete this comment block.
-->

<div align="center">

# Harsh Singh

### Full-Stack Developer

**React · Next.js · Node.js · MongoDB**

I build full-stack web apps with secure authentication, real-time features and clean APIs, and ship them to production.

<br>

[![Portfolio](https://img.shields.io/badge/Portfolio-harshsingh.netlify.app-2563EB?style=flat-square)](https://harshsingh.netlify.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square)](https://www.linkedin.com/in/YOUR-HANDLE) <!-- EDIT: your LinkedIn URL -->
[![Email](https://img.shields.io/badge/Email-Get%20in%20touch-24292F?style=flat-square)](mailto:YOUR-EMAIL) <!-- EDIT: your email -->

</div>

<br>

## About

I'm a full-stack developer based in India. My projects cover the whole path from UI to database to deployment: a Stripe-powered storefront, a real-time chat system with OTP-verified accounts, a document app with in-browser OCR, and a REST API with validation and business rules.

I care about **secure auth, validated input, documented APIs and responsive UI**, and I deploy what I build so people can try it.

- **Open to:** full-time and internship roles in full-stack development <!-- EDIT: change if different -->
- **Currently:** learning TypeScript and adding automated tests to my Node.js projects <!-- EDIT: keep only what is true -->

<br>

## Featured projects

<table>
<tr>
<td valign="top" width="50%">

#### [Real-Time Chat Application](https://github.com/harshcans/chat-application)

Secure messaging with verified accounts and live message delivery.

- Email OTP verification and JWT access + refresh tokens
- Socket.IO delivery with stored message history
- Membership checks on both REST and socket handlers
- Postman collection covering the full flow

`Node.js` `Express` `MongoDB` `Socket.IO` `JWT`

[Source code](https://github.com/harshcans/chat-application)

</td>
<td valign="top" width="50%">

#### [Educans](https://github.com/harshcans/educans)

Education-resources web app with in-browser PDF reading and OCR.

- PDF viewing with pdf.js
- Text extraction from images and documents with Tesseract.js
- Firebase and Supabase integrations for auth and storage
- Deployed on Vercel

`React` `pdf.js` `Tesseract.js` `Firebase` `Supabase`

[Live demo](https://educans.vercel.app/) · [Source code](https://github.com/harshcans/educans)

</td>
</tr>
<tr>
<td valign="top" width="50%">

#### [Amazon-v5](https://github.com/harshcans/Amazon-v5)

Full-stack e-commerce app built with Next.js.

- Google and Facebook sign-in
- Stripe payments at checkout
- User data stored in Firebase Firestore
- Fully responsive Tailwind UI

`Next.js` `React` `Tailwind CSS` `Firebase` `Stripe`

[Live demo](https://amazon-v5.vercel.app) · [Source code](https://github.com/harshcans/Amazon-v5)

</td>
<td valign="top" width="50%">

#### [LeetCode Progress Explorer](https://github.com/harshcans/leetcode-progress-tracker)

Dashboard to track LeetCode stats and compare with a rival.

- Difficulty breakdown, contest rating and topic-wise skill diagnostics
- Head-to-head comparison with any other handle
- Dark mode, glassmorphic UI, 7-day session via localStorage
- Fault-tolerant API fetching so the dashboard never crashes

`React` `Vite` `Tailwind CSS` `alfa-leetcode-api`

[Live demo](https://leetcode-track-progress.vercel.app) · [Source code](https://github.com/harshcans/leetcode-progress-tracker)

</td>
</tr>
<tr>
<td valign="top" width="50%">

#### [Event Management API](https://github.com/harshcans/Event-Management)

REST API for managing society events.

- Full CRUD with search, filtering, pagination and sorting
- Validation and business rules (no past events, no duplicates, completed events locked)
- Consistent error handling and HTTP status codes
- Postman collection and API documentation

`Node.js` `Express` `MongoDB` `Mongoose`

[Source code](https://github.com/harshcans/Event-Management)

</td>
<td valign="top" width="50%">

#### More work

Smaller experiments and learning projects live on my repositories page.

<br>

[Browse all repositories →](https://github.com/harshcans?tab=repositories)

</td>
</tr>
</table>

<details>
<summary><b>How the chat application works</b> (architecture)</summary>

<br>

```mermaid
sequenceDiagram
    autonumber
    participant C as Client
    participant API as Express REST API
    participant DB as MongoDB
    participant WS as Socket.IO

    C->>API: Register (name, email, password)
    API->>DB: Store user with hashed password
    API-->>C: Email OTP
    C->>API: Verify OTP, then log in
    API-->>C: JWT access + refresh tokens
    C->>API: Load conversations and message history
    C->>WS: Connect with access token
    C->>WS: joinConversation (membership checked)
    C->>WS: sendMessage
    WS-->>C: newMessage to everyone in the conversation
```

</details>

<br>

## Tech stack

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=js,react,nextjs,tailwind,vite,nodejs,express,mongodb,firebase,supabase,postman,git,vercel,netlify&perline=7&theme=dark">
  <source media="(prefers-color-scheme: light)" srcset="https://skillicons.dev/icons?i=js,react,nextjs,tailwind,vite,nodejs,express,mongodb,firebase,supabase,postman,git,vercel,netlify&perline=7&theme=light">
  <img alt="Tech stack: JavaScript, React, Next.js, Tailwind CSS, Vite, Node.js, Express, MongoDB, Firebase, Supabase, Postman, Git, Vercel, Netlify" src="https://skillicons.dev/icons?i=js,react,nextjs,tailwind,vite,nodejs,express,mongodb,firebase,supabase,postman,git,vercel,netlify&perline=7&theme=dark">
</picture>
</div>

<br>

| | |
|---|---|
| **Front end** | React · Next.js · Tailwind CSS · Vite · JavaScript (ES6+) · HTML/CSS |
| **Back end** | Node.js · Express · REST APIs · Socket.IO · JWT · bcrypt · Nodemailer |
| **Data and services** | MongoDB (Mongoose) · Firebase (Auth, Firestore) · Supabase · Stripe |
| **Tooling and deploy** | Git · GitHub · Postman · Vercel · Netlify |

<br>

## How I build

- **Security first:** hashed passwords, OTP-verified accounts, JWT access and refresh tokens, and authorization checks on real-time channels.
- **Reliable APIs:** input validation, consistent error handling, pagination, and documented endpoints with Postman collections.
- **Real-time features:** Socket.IO rooms with membership checks, backed by stored history.
- **Shipped, not just coded:** live demos on Vercel with responsive layouts and dark mode.

<br>

## Get in touch

Happy to talk about full-stack projects, open source or opportunities.

[Portfolio](https://harshsingh.netlify.app) · [LinkedIn](https://www.linkedin.com/in/YOUR-HANDLE) · [Email](mailto:YOUR-EMAIL) <!-- EDIT: same LinkedIn URL and email as above -->
