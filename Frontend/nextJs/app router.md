
## Basic Route

Next.js App Router uses the `app` folder for routing.

- Every folder creates a route.
    
- Every route must have a `page.tsx`.
    
- Folder names become the URL.
    

Example:

```text
app/
├── page.tsx
├── about/
│   └── page.tsx
└── contact/
    └── page.tsx
```

Routes:

```text
/
/about
/contact
```

---

## Nested Route

A folder inside another folder creates a nested route.

Example:

```text
app/
└── dashboard/
    ├── page.tsx
    ├── profile/
    │   └── page.tsx
    └── settings/
        └── page.tsx
```

Routes:

```text
/dashboard
/dashboard/profile
/dashboard/settings
```

Another example:

```text
app/
└── blog/
    ├── page.tsx
    └── posts/
        └── page.tsx
```

Routes:

```text
/blog
/blog/posts
```

---
