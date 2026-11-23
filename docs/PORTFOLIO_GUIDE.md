# Portfolio repository conventions

These conventions organize Ardeshir Rashidi's GitHub portfolio into two main areas: **Game Design & Development** and **Product Design**. A project's subject determines its area; its technology and output format are described separately.

## Categories and topics

| Main area | Required area topic | Focus topics when applicable |
| --- | --- | --- |
| Game Design & Development | `game-design` | `game-systems`, `game-research`, `game-design-documentation`, `game-ui-ux`, `game-prototype`, `simulation` |
| Product Design | `product-design` | `ux-design`, `ui-design`, `design-system`, `product-prototype`, `landing-page`, `dashboard`, `mobile-app` |

Choose one primary area based on the project's purpose and add the focus topics that describe the actual work. The profile's two collection links search by `game-design` and `product-design`.

### Game Design & Development

- **Gameplay Systems & Simulation:** mechanics, procedural systems, technical systems, and real-time simulations.
- **Game Research & Design Documentation:** research, mechanic studies, game design documents, specifications, balancing notes, and playtest findings.
- **Game UI/UX:** HUDs, menus, player feedback, player journeys, and interface design files.
- **Playable Prototypes:** playable tests and interactive demonstrations.

Outputs can include source design files, documents, Unreal Engine projects, or web builds. A browser-based game prototype belongs to this area because its subject is game design.

### Product Design

- **UX & Interaction Design:** research, information architecture, journeys, flows, wireframes, and usability studies.
- **UI & Design Systems:** visual interfaces, components, responsive layouts, and design-system files.
- **Interactive Product Prototypes:** landing pages, dashboards, and mobile application flows implemented as interactive front-end prototypes.

Next.js, React, TypeScript, HTML, CSS, and JavaScript describe implementation tools. A mobile UI demonstrated in a browser remains a mobile product prototype; it should not be described as a native application unless it actually is one.

### Technology and output topics

Add technologies only when the repository uses them, for example `unreal-engine-5`, `niagara-system`, `hlsl`, `cpp`, `nextjs`, `react`, or `typescript`. Describe the output explicitly in the README: design files, research/documentation, Unreal project, web prototype, or native build.

Examples:

| Project | Area topic | Focus topics | Technology topics |
| --- | --- | --- | --- |
| Niagara Ocean Simulation | `game-design` | `game-systems`, `simulation` | `unreal-engine-5`, `niagara-system`, `hlsl` |
| Game HUD design and prototype | `game-design` | `game-ui-ux`, `game-prototype` | Only the tools used by that project |
| Player research study | `game-design` | `game-research`, `game-design-documentation` | No engine topic unless an engine project is included |
| Product dashboard prototype | `product-design` | `dashboard`, `product-prototype` | `nextjs`, `react`, `typescript` when used |

## Repository names

Use short, descriptive, lowercase names with hyphens for new repositories.

- Product prototype: `<product>-prototype`, for example `zerolag-prototype`.
- Game system: `ue5-<system>`, for example `ue5-ocean-simulation`.
- Game research or documentation: `<subject>-game-research` or `<project>-game-design`.
- Game interface: `<project>-game-ui`.
- Reusable interface library: `<name>-design-system`.

Examples describe a naming pattern, not repositories that have already been published. A single prototype should have one repository; avoid creating separate repositories just to represent empty portfolio categories.

## Repository About section

Write a one-sentence description explaining what the project demonstrates. Put the working demo in the Website field when it exists. Use a short screenshot or recording in the README to help visitors understand the result quickly.

## Product prototype structure

Use the framework's normal structure. For a small HTML/CSS/JavaScript prototype:

```text
src/
  pages/
  components/
  styles/
  scripts/
public/
  images/
  icons/
docs/
  images/
README.md
```

For a Next.js prototype, follow the framework's [App Router conventions](https://nextjs.org/docs/app/getting-started): `src/app/` for routes and layouts, `src/components/` for shared UI, `src/lib/` for utilities, and `public/` for static assets. Add other directories when a concrete feature needs them.

The README should explain the design problem, your role, key flows, setup commands, demo behavior, and what is mocked. Distinguish a design prototype from a working authentication, payments, or production service implementation.

## Unreal Engine project structure

```text
Config/
Content/
Source/             # Only if the project contains C++ source
Plugins/            # Only if required
docs/
  images/
ProjectName.uproject
README.md
```

Document the tested engine version and required plugins. Do not commit `Binaries/`, `DerivedDataCache/`, `Intermediate/`, or `Saved/`. Use Git LFS for large binary Unreal assets when needed, with a reviewed `.gitattributes` configuration before the first asset commit.

## README checklist

Start with the [Game project template](../templates/GAME_PROJECT_README.md) or [Product design template](../templates/PRODUCT_DESIGN_README.md). The existing system and prototype templates are available for more specific technical projects.

1. State what the project is and why it exists.
2. Show the result with a preview or screenshot.
3. Explain your role and the design or system decisions.
4. Provide exact setup and run steps verified against the project.
5. List implemented features, mocked behavior, and known limitations.
6. Credit third-party assets and dependencies accurately.
7. State usage rights deliberately; public visibility alone is not a reuse license.

## Profile pins

Pin a small number of finished, representative projects. As the collection grows, show strong examples from both categories. Keep experiments available through the category links rather than filling the profile with unfinished placeholders.
