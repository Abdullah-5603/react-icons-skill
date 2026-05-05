# Next.js

React Icons are React components. Use them like ordinary React components in Next.js projects.

## App Router

Icons can be imported in Server Components if the surrounding component does not require client behavior:

```tsx
import { FiSearch } from "react-icons/fi";

export function EmptyState() {
  return (
    <div>
      <FiSearch aria-hidden="true" />
      <h2>No results</h2>
    </div>
  );
}
```

## When To Use `"use client"`

Use `"use client"` only when the component needs client-side behavior:

- React state.
- Effects.
- Browser APIs such as `window`, `document`, `localStorage`, or media queries implemented in JavaScript.
- Event handlers such as `onClick`, `onChange`, `onSubmit`, or keyboard handlers.
- Client-only library behavior.

Do not add `"use client"` only because a file imports an icon.

## Imports

Keep imports specific:

```tsx
import { FiSearch } from "react-icons/fi";
import { LuSettings } from "react-icons/lu";
import { SiGithub } from "react-icons/si";
```

Avoid broad or root imports. Specific subpackage imports are clearer and avoid accidental misuse.

## Dynamic Imports

Avoid dynamic import for normal icon usage. A static subpackage import is usually the simplest and most maintainable option.

Only consider dynamic import when:

- The icon is part of a rarely opened, heavy client-only surface.
- Profiling or bundle analysis shows a real performance issue.
- The codebase already uses a lazy-loading pattern for similar UI modules.

## Hydration

`react-icons` output is deterministic. Hydration problems around icons usually come from surrounding client-only behavior, theme initialization, random values, dates, or conditional rendering that differs between server and client.
