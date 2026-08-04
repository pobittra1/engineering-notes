

`layout.tsx` is used to share the same UI across multiple pages.

Instead of adding components like Navbar or Footer on every page, I can place them in `layout.tsx`.

---

## Example

```text
app/
├── layout.tsx
├── page.tsx
├── about/
│   └── page.tsx
└── contact/
    └── page.tsx
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