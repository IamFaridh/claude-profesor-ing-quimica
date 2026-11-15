# Tutor IA para Ingeniería Química

Manual para que una IA (Claude u otro modelo) te enseñe **por diálogo** temas de Ingeniería Química, calidad, inocuidad y seguridad: HACCP, BPM, POES, normas ISO, seguridad de procesos y más.

> **Basado en [claude-teach](https://github.com/diraneyya/claude-teach) de diraneyya** (v3.2, commit `ed7db1a`), publicado en dominio público. Esta versión es una adaptación independiente de **Faridh AF**; el autor original no participó en ella.

## Qué cambia respecto al original

- **Enfoque en Ingeniería Química y temas normativos:** se quitó el contenido de terminal y criptografía, y se agregó una sección para normas, calidad y seguridad, con el puente técnico de la IQ (cinética de inactivación, transferencia de calor, CIP, HAZOP…).
- **Modo fuente directa:** la IA responde y te dice dónde verificarlo, sin obligarte a buscar. El modo guiado sigue disponible.
- **Casos reales con escenarios hipotéticos**, con un punto de quiebre explícito entre lo real y lo hipotético.
- **Bitácora de la sesión:** registro de los temas estudiados durante todo el chat, con continuidad entre chats.
- **Práctica y simulacro:** evaluación con revisión previa y nota de 0 a 100.
- **Reglas de eficiencia:** respuestas breves por defecto para ahorrar tokens, sin perder la pedagogía.

## Uso

Copia este prompt al inicio de un chat nuevo:

```text
Actúa como mi tutor. El manual está en:
https://raw.githubusercontent.com/IamFaridh/claude-profesor-ing-quimica/main/CLAUDE.md
Léelo COMPLETO antes de empezar.

Tema de hoy: ...
Mi formación: Ingeniero Químico. Manejo ...
(Opcional) Me interesa ...                 (para enfocar la sesión)
(Opcional) Ya conozco / he usado ...       (para no repetir lo que sabes)
(Opcional) Prefiero un enfoque ...         (práctico, teórico, con casos…)
(Opcional) Mi objetivo final es ...        (entrevista, auditoría, trabajo…)
Contexto regulatorio: Perú
Tiempo para esta sesión: ...
```

Si la IA no puede abrir enlaces, adjunta el archivo `CLAUDE.md` en el chat en lugar de la URL.

### Ejemplo

```text
Tema de hoy: HACCP. Mi formación: Ingeniero Químico; manejo balances,
transferencia de calor y cinética. Me interesa aplicarlo a una línea de
bebidas. Ya conozco las BPM de forma general. Prefiero un enfoque con
casos. Mi objetivo final es poder armar un plan HACCP y defenderlo en una
entrevista. Contexto regulatorio: Perú.
Tiempo para esta sesión: 1 hora.
```

## Comandos

| Comando | Qué hace |
|---|---|
| `!ayuda` | Muestra la lista de comandos. |
| `!fuente` | Respuesta directa con su fuente (modo por defecto). |
| `!guiado` | La IA te orienta para que encuentres la fuente tú mismo. |
| `!breve` · `!normal` · `!detalle` | Cambia la extensión de las respuestas. |
| `!caso [tema]` | Caso real con extensión hipotética para resolver. |
| `!progreso` | Muestra la bitácora de temas estudiados. |
| `!continuar` | Genera un bloque para retomar la sesión en un chat nuevo. |
| `!practica [temas]` | Preguntas de práctica con retroalimentación inmediata, sin nota. |
| `!simulacro [temas]` | Evaluación con revisión previa y nota de 0 a 100. |

## Licencia

- **Material original de claude-teach:** dominio público ([Unlicense](https://unlicense.org)).
- **Adaptación, traducción y contenido nuevo:** © 2026 Faridh AF, bajo [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es). Puedes usarlo, modificarlo y compartirlo, incluso con fines comerciales, siempre que des crédito.

Atribución sugerida:

> "Tutor IA para Ingeniería Química" por Faridh AF, basado en claude-teach de diraneyya. Licencia CC BY 4.0.

Ver [LICENSE](LICENSE) para el texto completo.
