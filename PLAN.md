# Plan — "Implementing GitHub Copilot in Engineering Teams" · Checklist vivo

## Contexto

Deck Slidev de 14 slides para un team rollout de GitHub Copilot. 13 implementadas, 1 pendiente (slide 10).
La estructura se apoya en BIM2GO (Node.js + React) como caso real, presentado de forma anónima.

---

## Decisiones tomadas

- **Idioma**: Slides y speaker notes en inglés
- **Audiencia**: Equipo técnico
- **Aspecto**: 16:9
- **Animaciones**: Nativas Slidev (`fade-up`, `v-motion`) — sin librerías externas
- **Tipografía**: Geist Mono vía `@fontsource/geist-mono`
- **Paleta**: `#000` fondo · `#f5f5f5` texto primario · `#8d8d8d` secundario
- **Narrativa**: rollout realista basado en BIM2GO, anonimizado
- **Privacidad**: sin nombre del producto en slides, sin URLs internas, sin screenshots
- **Sin em dashes** en texto visible de slides
- **Componentes Vue** para layouts complejos (evita bugs del parser markdown de Slidev)
- **Demo 2**: agentes reales en `BIM2GO_backend/.github/agents/`, demo con `/fleet`

---

## Checklist

### Fase 0 — Base del proyecto
- [x] Mantener `_refs/` como fuente de contenido y referencias visuales
- [x] Mantener `PLAN.md` como checklist vivo y sincronizado
- [x] Confirmar stack Slidev y tipografía base

### Fase 1 — Reorientación editorial
- [x] Cambiar `_refs/guide.md` a rollout basado en BIM2GO
- [x] Caso base: repo con guidance parcial pero sin baseline Copilot
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
- [x] Slide 9: "Demo 1 — login button feedback: without /plan vs with /plan"
- [ ] Slide 10: "How to use /review"
- [x] Slide 11: "Skills and custom agents"
- [x] Slide 12: "Subagents"
- [x] Slide 13: "Demo 2 — Agents and fleet"
- [x] Slide 14: "Closing"

### Fase 3 — Notes y consistencia
- [ ] Speaker notes en todos los slides
- [ ] Speaker notes en inglés con frases cortas y sin modismos
- [ ] Revisar que ningún slide tenga em dashes en texto visible

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
│   ├── 01-why-shared-operating-model.md
│   ├── 02-how-copilot-works-in-practice.md
│   ├── 03-three-control-layers.md
│   ├── 04-what-enterprise-controls.md
│   ├── 05-real-repo-setup.md
│   ├── 06-what-each-repo-must-define.md
│   ├── 07-bad-vs-good-prompts.md
│   ├── 08-cli-patterns.md
│   ├── 09-how-to-use-plan.md
│   ├── 11-skills-and-custom-agents.md
│   ├── 12-subagents.md
│   └── 13-demo-agents-fleet.md
├── components/
│   ├── DeckFrame.vue
│   ├── SlideHeading.vue
│   ├── BulletStack.vue
│   ├── ControlMap.vue
│   ├── LayerBands.vue
│   ├── RepoSetupDiagram.vue
│   ├── PromptCompare.vue
│   ├── EditorWorkflowCard.vue
│   ├── DemoCompare.vue
│   ├── SkillsAgents.vue
│   ├── Subagents.vue
│   └── AgentSetup.vue
├── _refs/guide.md
├── style.css
└── PLAN.md
```

## Agentes de demo (BIM2GO)

```
BIM2GO_backend/.github/agents/
├── test-writer.agent.md    — Jest + Supertest tests para rutas Express
└── sql-reviewer.agent.md  — revisión SQL en modelos, HIGH / MEDIUM / INFO
```

Comando de demo: `/fleet "Review db/card.model.js for SQL safety AND write integration tests for the card routes."`
