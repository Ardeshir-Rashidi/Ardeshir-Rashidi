# Portfolio repository conventions

These conventions organize Ardeshir Rashidi's GitHub portfolio around interactive product prototypes and game systems. They are intended for new projects; existing repository URLs can stay stable.

## Categories and topics

| Category | Required category topic | Supporting topics when applicable |
| --- | --- | --- |
| Interactive product prototypes | `product-prototype` | `product-design`, `ui-design`, `interactive-prototype`, `design-system`, `html-css-javascript`, `react`, `nextjs` |
| Game systems and experiments | `game-systems` | `game-development`, `unreal-engine-5`, `niagara-system`, `simulation`, `procedural-generation`, `hlsl`, `cpp` |

Add technologies only when the repository actually uses them. Use one main category topic and a small set of specific topics. The profile's category links search for these topics, so newly tagged public repositories appear in the appropriate collection.

## Repository names

Use short, descriptive, lowercase names with hyphens for new repositories.

- Product prototype: `<product>-prototype`, for example `zerolag-prototype`.
- Game system: `ue5-<system>`, for example `ue5-ocean-simulation`.
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

1. State what the project is and why it exists.
2. Show the result with a preview or screenshot.
3. Explain your role and the design or system decisions.
4. Provide exact setup and run steps verified against the project.
5. List implemented features, mocked behavior, and known limitations.
6. Credit third-party assets and dependencies accurately.
7. State usage rights deliberately; public visibility alone is not a reuse license.

## Profile pins

Pin a small number of finished, representative projects. As the collection grows, show strong examples from both categories. Keep experiments available through the category links rather than filling the profile with unfinished placeholders.
