# React Firebase Auth Starter - TypeScript + Vite + Tailwind

<!-- MIT License -->

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)

<!-- HTML & CSS -->

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

<!-- Styling / PostCSS -->

[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/docs/)

<!-- Languages & Web Standards -->

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![ECMAScript Spec](https://img.shields.io/badge/ECMAScript-262-7A0BC0?logo=ecmascript&logoColor=white)](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178c6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/docs/)

<!-- Infra & Runtime -->

[![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)

<!-- Auth & Security -->

[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com/docs)

<!-- Linting & Formatting -->

[![ESLint](https://img.shields.io/badge/ESLint-4B32C3?logo=eslint&logoColor=white)](https://eslint.org/docs/latest/)
[![Prettier](https://img.shields.io/badge/Prettier-2B3A42?logo=prettier&logoColor=white)](https://prettier.io/docs/)

<!-- Bundler -->

[![Vite](https://img.shields.io/badge/Vite-646cff?logo=vite&logoColor=white)](https://vite.dev/)

## Plain docs links

- HTML (MDN) docs: [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- CSS (MDN) docs: [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- Tailwind CSS docs: [https://tailwindcss.com/docs/](https://tailwindcss.com/docs/)
- JavaScript (MDN) docs: [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- ECMAScript (spec, ECMA-262) docs: [https://www.ecma-international.org/publications-and-standards/standards/ecma-262/](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)
- TypeScript docs: [https://www.typescriptlang.org/docs/](https://www.typescriptlang.org/docs/)
- Node.js docs: [https://nodejs.org/](https://nodejs.org/)
- React docs: [https://react.dev/](https://react.dev/)
- Firebase docs: [https://firebase.google.com/docs](https://firebase.google.com/docs)
- ESLint docs: [https://eslint.org/docs/latest/](https://eslint.org/docs/latest/)
- Prettier docs: [https://prettier.io/docs/](https://prettier.io/docs/)
- Vite docs: [https://vite.dev/](https://vite.dev/)

---

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

### Contact & Maintainer

- **Project:** _react-vite-firebase-ts_
- **Name:** Md Abu Kayser - Full-Stack Engineer
- **Maintainer:** [md-abu-kayser](https://github.com/md-abu-kayser)
- **Email:** [abu.kayser.official@gmail.com](mailto:abu.kayser.official@gmail.com)
- **GitHub:** [github.com/abu.kayser-official](https://github.com/md-abu-kayser)

If you’d like this README tailored for a specific purpose - such as **hiring managers**, **open-source contributors**, or **client deliverables** - feel free to request a custom tone or format.

 **Thank you for reviewing this project!**

 ---
