# React Icons Skill

[![skills.sh](https://skills.sh/b/Abdullah-5603/react-icons-skill)](https://skills.sh/Abdullah-5603/react-icons-skill/react-icons)

An unofficial Agent Skill for helping coding agents use `react-icons` correctly in React, Next.js, Vite, CRA, JavaScript, and TypeScript projects.

This repository does not contain a React app and does not install `react-icons` itself. It only provides skill instructions, references, and evals for agents.

## Install

```sh
npx skills add https://github.com/Abdullah-5603/react-icons-skill --skill react-icons
```

## Local Install

```sh
npx skills add . --skill react-icons
```

## Codex Global Install

```sh
npx skills add https://github.com/Abdullah-5603/react-icons-skill --skill react-icons -g -a codex -y
```

## Expected Skills.sh Page

https://skills.sh/Abdullah-5603/react-icons-skill/react-icons

## What This Skill Helps With

- Installing `react-icons` with the right package manager.
- Fixing imports so icons come from subpackages such as `react-icons/fi`, `react-icons/fa`, or `react-icons/si`.
- Choosing icon families for React, Next.js, Vite, CRA, JavaScript, and TypeScript projects.
- Replacing inline SVGs with `react-icons` components.
- Applying accessibility rules for decorative icons, icon-only buttons, loading indicators, and status icons.
- Using `react-icons` in Next.js App Router projects without unnecessary client components.
- Writing TypeScript-friendly icon components and reusable icon button APIs.
- Styling icons with `className`, SCSS, Tailwind, design-system classes, and `currentColor`.

## Repository Contents

- `skills/react-icons/SKILL.md`: the main Agent Skill instructions.
- `skills/react-icons/references/`: focused reference docs for icon prefixes, accessibility, Next.js, and SVG migration.
- `skills/react-icons/evals/evals.json`: eval prompts for checking expected agent behavior.

## Contributing

Contributions are welcome. Before opening a pull request, read [CONTRIBUTING.md](CONTRIBUTING.md), follow the [Code of Conduct](CODE_OF_CONDUCT.md), and keep changes focused on the Agent Skill itself.

Useful contribution areas:

- Better `react-icons` usage examples.
- More framework-specific guidance for React, Next.js, Vite, CRA, JavaScript, and TypeScript.
- Accessibility improvements.
- Additional migration examples from inline SVGs.
- Eval coverage for common agent mistakes.

## Security

This repository contains documentation and skill instructions, not runtime application code. Still, please report sensitive issues using the guidance in [SECURITY.md](SECURITY.md).

## License

MIT. See [LICENSE](LICENSE).

## Unofficial

This is an unofficial community Agent Skill. It is not affiliated with, endorsed by, or maintained by the official React Icons project.
