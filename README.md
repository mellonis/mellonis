# Hi there 👋

📫 [mellonis.ru](https://www.mellonis.ru)

## Portfolio

- 📜 [Poetry website](https://poetry.mellonis.ru). Personal project — my own poems and prose, organized into themed sections, with bookmarks, comments, voting and full-text search. Migrated a long-running PHP site (the [previous version](https://old2.poetry.mellonis.ru) is still online) into a multi-stack architecture: a Next.js 16 / React 19 frontend and a Fastify / TypeScript API (JWT + WebAuthn passkeys, rate-limiting, structured logging) on MySQL 8 + Meilisearch. Self-hosted on a single VPS via Docker, nginx + Let's Encrypt, GitHub Actions deploys.

https://github.com/user-attachments/assets/90e3e7dc-14e2-4005-893c-270b1658711a

- 💳 [Yandex Pay](https://pay.yandex.ru) — web app + native-app webviews. React 18 + TypeScript + Apollo GraphQL + React Hook Form on the client; Express / Next.js / NestJS on the server side. Built the registration flow; led the dark-theme integration and Figma-token-driven CSS generation; advocated for currentColor-driven SVG icons across the team. Contributed to overall application architecture in close collaboration with backend. Owned most of the frontend for the multi-level KYC flows — Basic, mobileID + Gosuslugi (KycEds), and full identification (Kyc/Max) via either an offline courier visit (Yandex Maps polygons for zoom-aware delivery areas + pins, with the map's visible area recomputed as the drawer opens) or an online selfie verification through a native-camera deeplink — including architectural analysis and protocol review. Seamless webview integration: theme bridging, viewport safe-area handling so the map fills the screen under the notch / Dynamic Island while UI stays within the safe-area inset, and a GeoLocation API wrapper papering over iPhone quirks.

- 🥰 [Alex Glushko plastic surgeon website](https://alexglushko.ru/). React 17 + Redux + Sass on a CMS-fed page-block architecture — clients compose pages from typed blocks, each with configurable image/video positions and dynamic SVG generation. Content-driven popup architecture letting CMS authors trigger popups from inline links in body text, resolved against the page's registered popups by a section-scoped delegated click handler. Lottie + canvas animations choreographed by configurable scene sequences, scroll-tied dark/light theme, ResizeObserver-driven responsive SVGs, IntersectionObserver-driven active-section table of contents, text rendered along curve paths, Google Maps integration, CSS 3D transforms. Image/video lazy loading designed around the Chromium memory leak below. [Announcement](https://www.artlebedev.com/alexglushko/) on the Art. Lebedev Studio website.

https://github.com/user-attachments/assets/a0e36304-aab0-4f39-9463-9fe7253bfbe1

- 🏦 [Financial culture website](https://fincult.info). Financial calculators (loan, deposit, inflation) and the borrower-knowledge test — the parts I'm proudest of. Hand-rolled the loan and deposit mechanics engines (with unit tests, sharing an OperationsGenerator event-stream core): true interest accrual with out-of-schedule extra payments and withdrawals, both annuity and differential amortization, variable interest-rate history, monthly/quarterly/yearly schedules, weekend → Monday carry-over for due dates, deposit capitalization, banker's rounding. On the inflation calculator I built the "superfood" price-comparison mode. Plus dynamic SVG chart generation (with some d3 helpers), seeded-random SVG clip-path shapes for article card images, Leaflet maps, custom form controls with Inputmask + React Hook Form, YouTube embeds. React 16 + Redux. [Announcement](https://www.artlebedev.com/cbr/fincult/) on the Art. Lebedev Studio website.

- 🌾 [Agrobank Uzbekistan website](https://www.agrobank.uz/ru). Multi-language banking site on TypeScript + React 17 + Redux Toolkit + Sass. i18next-driven Russian/Uzbek routing, Yandex Maps for branch lookup, client-side PDF generation via @react-pdf/renderer, Storybook component library, Swiper carousels, react-helmet-async for SEO. [Announcement](https://www.artlebedev.com/agrobank/site/) on the Art. Lebedev Studio website.

## Open source

- 🤖 [machines-demo](https://demo.machines.mellonis.ru) Interactive in-browser playground for Turing and Post machines. Two tabs (Turing, Post) where you write JavaScript that builds a machine — using the published @turing-machine-js/machine and @post-machine-js/machine libraries — and watch it execute on an animated tape. Auto-running demo on first load, manual control of the tape head via a movement/symbol/Apply panel, single-step and paused-auto-step execution, and a log of every command applied. [Source](https://github.com/mellonis/machines-demo)

https://github.com/user-attachments/assets/82db4261-ca76-4db5-86db-e161df169b4a

- 🧮 [@turing-machine-js/machine](https://www.npmjs.com/package/@turing-machine-js/machine) — TypeScript Turing-machine simulator with a builder DSL and a binary-numbers library, published as an npm monorepo. [Source](https://github.com/mellonis/turing-machine-js).

- 🧠 [@post-machine-js/machine](https://www.npmjs.com/package/@post-machine-js/machine) — Post-Turing machine that compiles its compact instruction set (mark / erase / left / right / check) down to states of the Turing-machine simulator above. [Source](https://github.com/mellonis/post-machine-js).

## Found bugs

- A memory leak with lazy load images in Chromium browsers — https://bugs.chromium.org/p/chromium/issues/detail?id=1213045
