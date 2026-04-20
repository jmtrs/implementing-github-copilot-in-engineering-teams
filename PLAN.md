# Plan — "Implementing GitHub Copilot in Engineering Teams" · Checklist vivo

## Contexto

Deck Slidev de 14 slides para un team rollout de GitHub Copilot.  
La estructura fue reorientada para apoyarse en un monorepo real derivado de X, pero presentado de forma anónima y sin detalles privados.

---

## Decisiones tomadas

- **Idioma**: Slides y speaker notes en inglés
- **Audiencia**: Equipo técnico
- **Aspecto**: 16:9
- **Animaciones**: Nativas Slidev (`v-click`, `v-motion`) — sin librerías externas
- **Tipografía**: Geist Mono vía `@fontsource/geist-mono`
- **Paleta**: `#000` fondo · `#f5f5f5` texto primario · `#8d8d8d` secundario
- **Narrativa**: rollout realista sobre un repo anónimo pero específico
- **Privacidad**: sin nombre X en slides, sin URLs internas, sin payloads sensibles, sin screenshots del producto
- **Slides 9+10 fusionadas**: una sola slide de demo en vivo con flujo vertical (sin /plan vs con /plan socrático)

---

## Checklist

### Fase 0 — Base del proyecto
- [x] Mantener `_refs/` como fuente de contenido y referencias visuales
- [x] Mantener `PLAN.md` como checklist vivo y sincronizado
- [x] Confirmar stack Slidev y tipografía base

### Fase 1 — Reorientación editorial
- [x] Cambiar `_refs/guide.md` de repo genérico a rollout basado en un monorepo real
- [x] Cambiar el caso base de “repo sin setup” a “repo con guidance parcial pero sin baseline Copilot”
- [x] Reescribir demos para baseline + tarea cross-layer
- [x] Mantener el contenido anonimizado pero trazable a una estructura real

### Fase 2 — Deck
- [x] Cover slide
- [x] Slide 1: "Why this needs a shared AI operating model"
- [x] Slide 2: "How Copilot works in practice"
- [x] Slide 3: "Three control layers"
- [x] Slide 4: "What Enterprise and the organization control"
- [x] Slide 5: "What an AI repo setup looks like"
- [x] Slide 6: "What each repository must define"
- [x] Slide 7: "Bad prompts vs good prompts"
- [x] Slide 8: "The Copilot CLI patterns"
- [x] Slide 9: "Demo — login button feedback: without /plan vs with /plan" (fusiona guía 9+10)
- [ ] Slide 10: "How to use review and verification"
- [ ] Slide 11: "Skills, custom agents, and subagents"
- [ ] Slide 12: "What quality and safety mean here"
- [ ] Slide 13: "Demo 2 and next steps"

### Fase 3 — Notes y consistencia
- [ ] Speaker notes en todos los slides
- [ ] Speaker notes en inglés con frases cortas y sin modismos
- [ ] Referencias explícitas a `.github/copilot-instructions.md`, `.github/instructions/*.instructions.md` y `AGENTS.md` en la guía
- [ ] Comandos del baseline alineados con frontend y backend reales

### Fase 4 — Verificación
- [ ] Probar modo presentación completo (`npm run dev`)
- [ ] Verificar visualmente el deck completo
- [ ] Ejecutar build del deck (`npm run build`)
- [ ] Exportar PDF de respaldo (`npm run export`)

---

## Estructura del proyecto

```
├── slides.md
├── slides/
│   ├── 00-cover.md
│   ├── 01-why-shared-rollout.md
│   ├── 02-what-copilot-changes.md
│   ├── ...
│   └── 14-next-steps.md
├── _refs/guide.md
├── style.css
├── components/
└── PLAN.md
```

