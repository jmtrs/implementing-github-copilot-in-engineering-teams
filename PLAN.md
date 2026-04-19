# Plan — "Implementing GitHub Copilot in Engineering Teams" · Checklist vivo

## Contexto

Deck Slidev de 18 slides para un team rollout de GitHub Copilot.  
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
- [ ] Slide 1: "Why this needs a shared AI operating model"
- [ ] Slide 2: "How Copilot works in practice"
- [ ] Slide 3: "Three control layers"
- [ ] Slide 4: "What Enterprise and the organization control"
- [ ] Slide 5: "What Enterprise does not solve"
- [ ] Slide 6: "What a real repo setup looks like"
- [ ] Slide 7: "The baseline we assume is already mounted"
- [ ] Slide 8: "What each repository still must define"
- [ ] Slide 9: "What good prompting looks like"
- [ ] Slide 10: "What bad prompting looks like"
- [ ] Slide 11: "The CLI patterns and capabilities that matter daily"
- [ ] Slide 12: "How to use `/plan` well"
- [ ] Slide 13: "How to use review and verification well"
- [ ] Slide 14: "Skills, custom agents, and subagents"
- [ ] Slide 15: "What quality and safety mean here"
- [ ] Slide 16: "What changes if other AI tools are also allowed"
- [ ] Slide 17: "Demo 1: from bad prompt to good prompt"
- [ ] Slide 18: "Demo 2 and next steps"

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

---

**Estado actual**: cover y slides 1 creada;
