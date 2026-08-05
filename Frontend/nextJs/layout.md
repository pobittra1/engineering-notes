`layout.tsx` is used to share the same UI across multiple pages.

Instead of adding components like Navbar or Footer on every page, I can place them in `layout.tsx`.

---

## Example

```text
app/
|- layout.tsx
|- page.tsx
|- about/
  |- page.tsx
|- contact/
    |- page.tsx
```

The layout is shared by all pages inside the `app` folder.

---

## Nested Layout

A folder can have its own layout.

```text
app/
└── dashboard/
    ├── layout.tsx
    ├── page.tsx
    └── settings/
        └── page.tsx
```

Both `/dashboard` and `/dashboard/settings` use the same dashboard layout.

---

## Notes

- Share common UI between pages.
- Avoid repeating the same components.
- Nested folders can have their own layouts.

# React `children` Notes

## Why use `children`?

- Reuse components
- Create flexible layouts
- Wrap page content
- Avoid repeating the same UI

---

## Syntax

```tsx
function Layout({ children }: { children: React.ReactNode }) {
  return <main>{children}</main>;
}
```

---

## Example

```tsx
function Layout({ children }: { children: React.ReactNode }) {
  return (
    <div>
      <h1>My Website</h1>
      {children}
    </div>
  );
}
```

Using the component:

```tsx
<Layout>
  <p>Welcome to my website!</p>
</Layout>
```

Output:

```html
<div>
  <h1>My Website</h1>
  <p>Welcome to my website!</p>
</div>
```

---

## In Next.js

In `layout.tsx`, `children` represents the current page or nested layout being rendered.

Example:

```tsx
export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```

---

## Key Points

- `children` is a built-in React prop.
- It contains the content inside a component.
- It makes components reusable and flexible.
- It is commonly used in layouts, wrappers, modals, cards, and providers.
- In Next.js, every `layout.tsx` should render `{children}` so that nested pages can be displayed.
