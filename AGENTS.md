# AGENTS.md — Implementing GitHub Copilot in Engineering Teams

## Proyecto

Deck Slidev de ~14 slides para un team rollout de GitHub Copilot.

## Idioma y audiencia

Documentado en `_refs/guide.md` (línea 12): *"simple enough for a Spanish-speaking audience using English at work"*.

- **Slides**: inglés (todo el texto visible en pantalla)
- **Speaker notes**: inglés, pero frases cortas y sin modismos — pensadas para ser leídas en voz alta por un castellanoparlante
- **Esta conversación**: el usuario habla en castellano; responder siempre en castellano

## Objetivo de la presentación

No es un demo de producto. Es un plan de rollout:
1. Qué controla la organización
2. Qué define cada repositorio
3. Cómo estandarizar el workflow del equipo
4. Qué cambia si se usan otras herramientas AI (Codex, Codex)
5. Próximos pasos concretos

## Stack técnico

- Slidev (`@slidev/cli`) con tema default
- Tipografía: Geist Mono (`@fontsource/geist-mono`)
- Paleta: fondo `#000`, texto primario `#f5f5f5`, secundario `#8d8d8d`
- Animaciones: `v-click`, `v-motion` nativas de Slidev — sin librerías externas
- Aspecto: 16:9

## Estructura de archivos

```
slides/          # Un .md por slide (00-cover.md, 01-…, etc.)
components/      # Componentes Vue reutilizables
_refs/           # Fuentes de contenido y referencia visual (no van al build)
style.css        # Variables globales de color y fuente
PLAN.md          # Checklist de progreso
```

## Fuentes de contenido

- `_refs/guide.md` — documento de trabajo con estructura de slides y notas
- `_refs/release-pipeline-animation.html` — referencia visual (SVG, animaciones)
- `_refs/release-pipeline-outro.html` — referencia visual (tipografía, cursor parpadeante)

## Normas de trabajo

- Los speaker notes van en el bloque `<!-- -->` al final de cada slide, con párrafos separados por línea en blanco
- En los speaker notes no añadir etiquetas ni marcadores (sin *intro*, *context*, ni similares)
- **No crear ningún archivo** (slides, componentes, docs) sin que el usuario lo pida explícitamente
- Antes de proponer texto para un slide, revisar `_refs/guide.md` para ese slide
- Todo el contenido de slides debe seguir `_refs/guide.md` como fuente de verdad
- **`PLAN.md` es el checklist vivo del proyecto**: actualizar cada ítem en cuanto se complete; nunca dejar `PLAN.md` desincronizado respecto al estado real del repo
