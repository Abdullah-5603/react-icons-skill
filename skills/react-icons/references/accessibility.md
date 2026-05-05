# Accessibility

Use icons according to their purpose, not their appearance.

## Decorative Icon Pattern

If visible text already communicates the meaning, hide the icon from assistive technology:

```tsx
import { FiSearch } from "react-icons/fi";

export function SearchLabel() {
  return (
    <span className="label-with-icon">
      <FiSearch aria-hidden="true" />
      <span>Search</span>
    </span>
  );
}
```

Short decorative form:

```tsx
<FiSearch aria-hidden="true" />
```

## Icon With Visible Text Pattern

For links and buttons with visible text, the text usually provides the accessible name:

```tsx
import { FiDownload } from "react-icons/fi";

export function DownloadButton() {
  return (
    <button type="button">
      <FiDownload aria-hidden="true" />
      <span>Download report</span>
    </button>
  );
}
```

## Icon-Only Button Pattern

Icon-only controls need an accessible name on the control:

```tsx
import { FiSearch } from "react-icons/fi";

export function SearchButton() {
  return (
    <button type="button" aria-label="Search">
      <FiSearch aria-hidden="true" />
    </button>
  );
}
```

Do not rely on the icon component's visual shape to name the button.

## Title Is Not Enough

Do not use `title` as the only accessible name for an icon-only button. Browser and assistive technology support is inconsistent, and `title` often does not work well for touch users.

Prefer:

```tsx
<button type="button" aria-label="Close">
  <FiX aria-hidden="true" />
</button>
```

## Loading And Spinner Icons

For loading indicators:

- If the button text changes to "Loading", "Saving", or "Submitting", keep the spinner decorative with `aria-hidden="true"`.
- If there is no visible loading text, add a screen-reader label or status text.
- Prefer `aria-busy="true"` on the affected region when content is being updated.
- Do not rely on animation alone to communicate progress.

Example:

```tsx
import { FiLoader } from "react-icons/fi";

export function SavingButton() {
  return (
    <button type="button" disabled>
      <FiLoader aria-hidden="true" className="spinner" />
      <span>Saving</span>
    </button>
  );
}
```

## Status Icons

Success, error, and warning icons must include text. Do not communicate status through icon shape or color alone.

```tsx
import { FiAlertTriangle } from "react-icons/fi";

export function ErrorMessage() {
  return (
    <p className="form-error">
      <FiAlertTriangle aria-hidden="true" />
      <span>Email address is required.</span>
    </p>
  );
}
```
