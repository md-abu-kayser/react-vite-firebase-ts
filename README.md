# React Firebase Auth Starter - TypeScript + Vite + Tailwind

A minimal, production-ready starter for React + TypeScript + Vite + Tailwind + Firebase Authentication. Clean architecture and clear examples make this repository ideal for demos, prototypes, or production bootstraps.

## Key highlights:

- Vite 4 + React 18 with TypeScript
- TailwindCSS for utility-first styling
- Firebase Authentication (Google and GitHub) wired in a compact example
- Opinionated linting and strict TypeScript settings
- Small, focused component layout for learning and extension

---

## Live structure

- Application entry: [src/main.tsx](src/main.tsx) - uses [`Main`](src/layout/Main.tsx)
- Main layout: [src/layout/Main.tsx](src/layout/Main.tsx) - exports [`Main`](src/layout/Main.tsx)
- Pages / components:
  - Home page: [src/component/Home/Home.tsx](src/component/Home/Home.tsx) - exports [`Home`](src/component/Home/Home.tsx)
  - Login page: [src/component/Login/Login.tsx](src/component/Login/Login.tsx) - exports [`Login`](src/component/Login/Login.tsx)
  - Header: [src/component/Header/Header.tsx](src/component/Header/Header.tsx) - exports [`Header`](src/component/Header/Header.tsx)
- Firebase init and auth instance: [src/firebase/firebase.init.ts](src/firebase/firebase.init.ts) - exports [`auth`](src/firebase/firebase.init.ts)
- Types: [src/types/index.ts](src/types/index.ts) - exports [`UserProfile`](src/types/index.ts), [`AuthContextType`](src/types/index.ts)
- Styling: [src/index.css](src/index.css)
- Tooling and config:
  - [package.json](package.json) (dev scripts and deps)
  - [vite.config.ts](vite.config.ts) (aliases and plugins)
  - [tsconfig.json](tsconfig.json) (strict TS setup)
  - [tailwind.config.js](tailwind.config.js)

---

## Features

- Client-side routing with `react-router-dom` configured in [src/main.tsx](src/main.tsx).
- Firebase Authentication:
  - Google and GitHub login flows implemented in [src/component/Login/Login.tsx](src/component/Login/Login.tsx) using [`auth`](src/firebase/firebase.init.ts).
  - Simple user profile management using the typed interfaces [`UserProfile`](src/types/index.ts) and [`AuthContextType`](src/types/index.ts).
- Minimal, responsive UI using Tailwind CSS (configured in [tailwind.config.js](tailwind.config.js)).
- Strict TypeScript and ESLint rules for maintainable code ([tsconfig.json](tsconfig.json), [.eslintrc.cjs](.eslintrc.cjs)).

---

## Quick start

### Prerequisites:

- Node 18+ recommended
- npm (or yarn/pnpm)

### Install and run locally:

1. **Install deps:**

```

npm install

```

2. **run build :**

```
npm run build

```

3. **Start dev server:**

```
npm run dev

```

### Available scripts

- dev - start Vite dev server
- build - run TypeScript checks and build with Vite
- preview - locally preview the production build
- lint - ESLint run (strict rules)
- type-check - full TypeScript check

### Authentication details

1. Firebase is initialized in src/firebase/firebase.init.ts. The exported auth instance is used by the login component to sign in with popup providers.
2. Login flows are implemented in src/component/Login/Login.tsx and demonstrate:
3. Login flows are implemented in src/component/Login/Login.tsx and demonstrate:

- Google sign-in (GoogleAuthProvider)
- GitHub sign-in (GithubAuthProvider)
- Handling onAuthStateChanged and basic profile display
  "These examples are intentionally unopinionated so you can integrate them into an Auth Provider or global context that uses the typed interfaces UserProfile and AuthContextType."

### Recommended production considerations

- Move Firebase config to environment variables and Vite env files (.env) instead of hard-coding.
- Add stricter session handling and refresh logic if you plan to persist auth across tabs or servers.
- Implement a central Auth Context/provider that surfaces typed state using AuthContextType.
- Apply route guards (RequireAuth) for protected routes.
- Add unit and E2E tests (Jest / React Testing Library / Playwright).

### Contributing

- Fork the repo and open a pull request with clear changelog and small commits.
- Keep components small and typed. Maintain the existing linting and formatting rules.
- For new features, add a small demo page under src/component/ and register it in the router (src/main.tsx).

### Appendix - Useful links in this repo

- Entry point: src/main.tsx
- Main layout: Main
- Pages: Home, Login
- UI: Header
- Firebase instance: auth
- Types: UserProfile, AuthContextType
- Configs: vite.config.ts, tsconfig.json, tailwind.config.js, .eslintrc.cjs

### License

- This project is licensed under the terms of the **[MIT License](./LICENSE)**.
- You may replace or update the license as needed for client or proprietary projects.

---

### Contact and Maintainer

**Maintainer:** [md-abu-kayser](https://github.com/md-abu-kayser)  
**Name:** Md Abu Kayser - Full-Stack Engineer

- **GitHub:** [github.com/abu.kayser-official](https://github.com/md-abu-kayser)
- **Email:** [abu.kayser.official@gmail.com](mailto:abu.kayser.official@gmail.com)
- **Project:** _react-firebase-starter-ts_

If you’d like this README tailored for a specific purpose - such as **hiring managers**, **open-source contributors**, or **client deliverables** - feel free to request a custom tone or format.

---

## **Thank you for reviewing this project!**
