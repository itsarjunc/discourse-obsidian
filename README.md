# Discourse Obsidian

A premium dark-first Discourse theme with layered near-black surfaces, Epic blue (`#0078f2`) accent, and a [shadcn/ui](https://ui.shadcn.com/docs/theming)-inspired CSS variable token architecture.

![Dark Theme](https://img.shields.io/badge/mode-dark--first-0a0a0b?style=flat-square&labelColor=0a0a0b&color=0078f2)
![Discourse](https://img.shields.io/badge/platform-Discourse-0078f2?style=flat-square)

## Features

- **Dark-first design** — near-black layered surfaces with light-mode fallback
- **Epic blue accent** (`#0078f2`) across all interactive elements
- **Inter** font via Google Fonts
- **shadcn/ui token system** — semantic CSS variable pairs (`background`/`foreground`, `card`, `popover`, `muted`, `accent`, `border`, `input`, `ring`)
- **Zero hardcoded hex** in component styles — every color flows through CSS custom properties
- **Frosted glass header** with `backdrop-filter` (toggleable via settings)
- **Full coverage**: sidebar, category page, topic list, post stream, composer, modals, dropdowns, buttons, and inputs

## Installation

1. Push this repo to a git host (GitHub, GitLab, etc.)
2. In Discourse admin: **Admin → Themes → Install → From a git repository**
3. Paste the repo URL and install
4. Go to **Admin → Themes** and select **Discourse Obsidian**
5. Set **obsidian-dark** as the active color palette

## Theme Settings

| Setting | Type | Default | Description |
|---------|------|---------|-------------|
| `obsidian_accent_color` | color | `#0078f2` | Primary accent color |
| `obsidian_border_radius` | string | `0.5rem` | Base border radius for UI elements |
| `obsidian_frosted_header` | boolean | `true` | Enable frosted glass header effect |

## Color Schemes

Two bundled color schemes are registered automatically on install:

| Scheme | Base | Text | Accent | Header |
|--------|------|------|--------|--------|
| **obsidian-dark** | `#0a0a0b` | `#e4e4e7` | `#0078f2` | `#0f0f11` |
| **obsidian-light** | `#fafafa` | `#18181b` | `#0078f2` | `#ffffff` |

## Architecture

```
discourse-obsidian/
├── about.json                  # Metadata + color schemes
├── settings.yml                # Admin-editable settings
├── locales/en.yml              # Locale strings
├── common/
│   ├── common.scss             # Entry (imports all partials)
│   └── head_tag.html           # Google Fonts preload
└── stylesheets/
    ├── obsidian-tokens.scss    # CSS variable token system
    ├── obsidian-base.scss      # Globals: font, scrollbar, links
    ├── obsidian-header.scss    # Header + frosted glass
    ├── obsidian-sidebar.scss   # Sidebar navigation
    ├── obsidian-categories.scss
    ├── obsidian-topic-list.scss
    ├── obsidian-post-stream.scss
    ├── obsidian-composer.scss
    ├── obsidian-modals.scss
    ├── obsidian-buttons.scss
    └── obsidian-forms.scss
```

## License

Proprietary — All Rights Reserved. See [LICENSE](./LICENSE).
