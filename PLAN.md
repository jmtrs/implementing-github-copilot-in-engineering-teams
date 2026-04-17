# Plan — "Implementing GitHub Copilot in Engineering Teams" · Checklist vivo

## Contexto

Deck Slidev de 13-14 slides para un team rollout de GitHub Copilot.  
Contenido: `_refs/using-github-copilot-well_working-document.md`  
Estilo visual (colores, tipografía, animaciones): `_refs/release-pipeline-*.html`

---

## Decisiones tomadas

- **Idioma**: Inglés (audiencia trabaja en inglés)
- **Aspecto**: 16:9
- **Animaciones**: Nativas Slidev (`v-click`, `v-motion`) — sin anime.js
- **Tipografía**: Geist Mono vía `@fontsource/geist-mono`
- **Paleta**: `#000` fondo · `#f5f5f5`/`#fff` texto primario · `#8d8d8d` secundario

---

## Checklist

### Fase 0 — Reorganizar el repo
- [x] Crear carpeta `_refs/`
- [x] Mover `release-pipeline-animation.html` → `_refs/`
- [x] Mover `release-pipeline-outro.html` → `_refs/`
- [x] Mover `using-github-copilot-well_working-document.md` → `_refs/`
- [x] Actualizar `PLAN.md` como checklist vivo

### Fase 1 — Scaffold Slidev
- [x] `package.json` con `@slidev/cli`, `@slidev/theme-default`, `@fontsource/geist-mono`
- [x] `slides.md` con frontmatter mínimo (tema, aspecto, fuente)
- [x] `styles/global.css` con variables de color y fuente base
- [x] `components/` (carpeta vacía)
- [x] Verificar: `npx slidev` abre cover slide sin errores

### Fase 2 — Cover slide (Slide 0)
- [x] Título: "Implementing GitHub Copilot in Engineering Teams"
- [x] Subtítulo: "Shared setup, workflow, and guardrails"
- [x] Estilo: fondo negro, Geist Mono, animaciones fade-in escalonadas
- [x] Verificar visualmente en navegador
- [x] Speaker notes del cover redactadas y aprobadas

### Fase 3 — Slides de contenido (1–13)
- [ ] Slide 1: "Why we need a shared AI setup"
- [ ] Slide 2: "What GitHub Copilot and Copilot CLI are"
- [ ] Slide 3: "Three control layers (Org → Repo → Local)"
- [ ] Slide 4: "What the organization can control"
- [ ] Slide 5: "What the repository can control"
- [ ] Slide 6: "Minimum setup for repos with no AI configuration"
- [ ] Slide 7: "Demo 1 — Initialize repo baseline"
- [ ] Slide 8: "Team workflow to standardize"
- [ ] Slide 9: "Quality, security, and real limits"
- [ ] Slide 10: "Can we allow Codex or Claude?"
- [ ] Slide 11: "What changes with mixed AI tools"
- [ ] Slide 12: "Demo 2 — Show standard workflow"
- [ ] Slide 13: "Recommendation and next steps"
- [ ] Slide 14: "Thanks." *(cierre, patrón de `release-pipeline-outro.html`)*

### Fase 4 — Componentes visuales
- [ ] `ControlLayers.vue` — diagrama Org → Repo → Local
- [ ] `WorkflowSteps.vue` — pasos del team workflow con `v-click`
- [ ] `BlinkingCursor.vue` — reutilizable en cover y cierre

### Fase 5 — Pulido final
- [ ] Speaker notes en todos los slides
- [ ] Animaciones de entrada con `v-motion` en slides clave
- [ ] Probar modo presentación completo (`npx slidev --open`)
- [ ] Exportar PDF de respaldo (`npx slidev export`)

---

## Estructura del proyecto

```
├── slides.md               # Entrada: frontmatter global + imports
├── slides/                 # Un archivo .md por slide
│   ├── 00-cover.md
│   ├── 01-why-shared-setup.md
│   └── ...
├── style.css               # Cargado automáticamente por Slidev (Geist Mono + paleta)
├── components/             # Componentes Vue reutilizables
│   ├── ControlLayers.vue
│   ├── WorkflowSteps.vue
│   └── BlinkingCursor.vue
├── _refs/                  # Archivos de referencia (no van al build)
├── package.json
└── PLAN.md
```

## Archivos críticos

| Archivo | Rol |
|---|---|
| `_refs/using-github-copilot-well_working-document.md` | Fuente de contenido |
| `_refs/release-pipeline-animation.html` | Referencia visual (SVG, animaciones) |
| `_refs/release-pipeline-outro.html` | Referencia visual (tipografía, cursor) |
| `slides.md` | Entrada del deck (frontmatter + imports) |
| `slides/*.md` | Un archivo por slide |
| `style.css` | Geist Mono + variables de color globales |
| `components/*.vue` | Componentes de diagrama reutilizables |

---

**Estado actual**: Fase 3 — Slides de contenido (siguiente: Slide 1)
