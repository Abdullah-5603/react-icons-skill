# Contributing

Thanks for helping improve the unofficial React Icons Agent Skill.

This repository is intentionally small. It does not contain a React app, build system, package manifest, or installed copy of `react-icons`. Contributions should improve the skill instructions, references, evals, or open-source maintenance files.

## Project Scope

Good contributions include:

- Clearer guidance for using `react-icons` in React, Next.js, Vite, CRA, JavaScript, or TypeScript projects.
- Better examples for imports, accessibility, styling, and inline SVG migration.
- Corrections to icon family names, prefixes, or package paths.
- New eval cases in `skills/react-icons/evals/evals.json`.
- Documentation improvements that keep the unofficial status clear.

Out of scope:

- Creating a React demo app inside this repository.
- Installing `react-icons` or adding a package manager lockfile.
- Claiming official affiliation with the React Icons project.
- Adding generated local agent install artifacts such as `.agents/`, `.claude/`, or `skills-lock.json`.

## Local Checks

Run these checks before opening a pull request:

```sh
test -f skills/react-icons/SKILL.md
grep -q '^name: react-icons$' skills/react-icons/SKILL.md
grep -q '^description:' skills/react-icons/SKILL.md
grep -q 'official: false' skills/react-icons/SKILL.md
jq empty skills/react-icons/evals/evals.json
```

Also check that correct examples import from subpackages such as `react-icons/fi`, `react-icons/fa`, `react-icons/fa6`, `react-icons/lu`, and `react-icons/si`.

The root import below should only appear as an incorrect example:

```tsx
import { FaGithub } from "react-icons";
```

## Writing Guidelines

- Be practical and copy-pasteable.
- Prefer concrete examples over broad advice.
- Keep accessibility behavior explicit.
- Mention package-manager detection before install commands.
- Keep the skill unofficial in wording and metadata.
- Do not add dependencies unless there is a clear maintenance reason.

## Pull Request Checklist

- The skill folder remains `skills/react-icons`.
- The skill name remains `react-icons`.
- `SKILL.md` frontmatter remains valid.
- No correct example imports icons from the root `react-icons` package.
- Any new eval object includes `id`, `prompt`, and `expected_behavior`.
- The repo still has no application scaffold or dependency install.

By contributing, you agree that your contribution will be licensed under the MIT License.
