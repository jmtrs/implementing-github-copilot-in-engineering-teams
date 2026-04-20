# Implementing GitHub Copilot in Engineering Teams

A Slidev presentation deck for rolling out GitHub Copilot across an engineering organization. Covers the three-layer control model (Enterprise, organization, repository), standardized team workflows, prompt patterns, CLI skills, and custom agents.

A PDF export is included at the root of this repository.

---

## Run locally

```bash
pnpm install
pnpm dev
```

Opens the deck at `http://localhost:3030`.

## Build

```bash
pnpm build    # static output in dist/
pnpm export   # PDF export
```

## Structure

| Path | Contents |
|---|---|
| `slides/` | One `.md` file per slide (`00-cover.md` … `14-closing.md`) |
| `components/` | Reusable Vue components for complex layouts |
| `style.css` | Global color and typography variables |
| `slides.md` | Slidev entry point and configuration |
| `_refs/` | Source material and visual references (not included in build) |

## Stack

- [Slidev](https://sli.dev) — presentation framework
- [Geist Mono](https://vercel.com/font) via `@fontsource/geist-mono`
- Color palette: `#000` background, `#f5f5f5` primary text, `#8d8d8d` secondary
