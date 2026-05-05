# Migration Examples

Use these examples when replacing inline SVGs or one-off icon components with `react-icons`.

## Inline Search SVG To FiSearch

Before:

```tsx
export function SearchInput() {
  return (
    <label className="search-input">
      <svg className="search-input__icon" viewBox="0 0 24 24" aria-hidden="true">
        <path d="M21 21l-4.3-4.3" />
        <circle cx="11" cy="11" r="7" />
      </svg>
      <input type="search" placeholder="Search" />
    </label>
  );
}
```

After:

```tsx
import { FiSearch } from "react-icons/fi";

export function SearchInput() {
  return (
    <label className="search-input">
      <FiSearch className="search-input__icon" aria-hidden="true" />
      <input type="search" placeholder="Search" />
    </label>
  );
}
```

## Inline Close SVG To FiX

Before:

```tsx
export function CloseButton({ onClose }: { onClose: () => void }) {
  return (
    <button type="button" className="modal__close" aria-label="Close" onClick={onClose}>
      <svg viewBox="0 0 24 24" aria-hidden="true">
        <path d="M18 6 6 18M6 6l12 12" />
      </svg>
    </button>
  );
}
```

After:

```tsx
import { FiX } from "react-icons/fi";

export function CloseButton({ onClose }: { onClose: () => void }) {
  return (
    <button type="button" className="modal__close" aria-label="Close" onClick={onClose}>
      <FiX aria-hidden="true" />
    </button>
  );
}
```

## Brand GitHub SVG To SiGithub Or FaGithub

Prefer Simple Icons when the brand mark matters:

```tsx
import { SiGithub } from "react-icons/si";

export function GithubBrandLink() {
  return (
    <a href="https://github.com/example" className="brand-link">
      <SiGithub aria-hidden="true" />
      <span>GitHub</span>
    </a>
  );
}
```

Use Font Awesome if the surrounding project already uses Font Awesome icons:

```tsx
import { FaGithub } from "react-icons/fa";

export function GithubLink() {
  return (
    <a href="https://github.com/example" className="brand-link">
      <FaGithub aria-hidden="true" />
      <span>GitHub</span>
    </a>
  );
}
```

## Sidebar Menu Icons Migrated To One Family

Before:

```tsx
import { FaHome } from "react-icons/fa";
import { FiSettings } from "react-icons/fi";
import { MdPeople } from "react-icons/md";

export const navItems = [
  { label: "Home", icon: FaHome },
  { label: "Team", icon: MdPeople },
  { label: "Settings", icon: FiSettings },
];
```

After:

```tsx
import { LuHome, LuSettings, LuUsers } from "react-icons/lu";

export const navItems = [
  { label: "Home", icon: LuHome },
  { label: "Team", icon: LuUsers },
  { label: "Settings", icon: LuSettings },
];
```

## BEM/SCSS ClassName Preservation

Before:

```tsx
export function SidebarToggle() {
  return (
    <button type="button" className="sidebar-toggle" aria-label="Open sidebar">
      <svg className="sidebar-toggle__icon" viewBox="0 0 24 24" aria-hidden="true">
        <path d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>
  );
}
```

After:

```tsx
import { FiMenu } from "react-icons/fi";

export function SidebarToggle() {
  return (
    <button type="button" className="sidebar-toggle" aria-label="Open sidebar">
      <FiMenu className="sidebar-toggle__icon" aria-hidden="true" />
    </button>
  );
}
```

Existing SCSS can usually stay focused on layout, color, and size:

```scss
.sidebar-toggle__icon {
  width: 20px;
  height: 20px;
  color: currentColor;
}
```
