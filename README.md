# Soluciones Integrales

Landing + configurador 3D de racks. Parte de GRUPO ISARACK.

- `index.html` — Landing
- `configurador.html` — Configurador 3D (Góndola / Picking / Selectivo)

Desplegado en Vercel desde `main`.

---

## Reglas de obra que el configurador debe respetar

Estas reglas vienen del taller. Si algún cambio al código las rompe, la lista de materiales que sale al cliente queda mal y le entregamos piezas que no cargan.

### Rejilla electrosoldada selectivo (SEL)

La rejilla viene en 2 anchos y NO son intercambiables entre largos de viga:

| Largo de viga | Ancho de rejilla | # por nivel |
|---|---|---|
| 96"  | 46" | 2 |
| 108" | **52"** | 2 |
| 144" | 46" | 3 |

SKUs disponibles en el inventario ISA-OS:

| Fondo del marco | Ancho 46" | Ancho 52" |
|---|---|---|
| 36" | SEL-0273 | SEL-0274 |
| 42" | SEL-0275 | SEL-0276 |
| 48" | SEL-0277 | SEL-0279 |

En código: `REJILLAS_SEL[fondoIn][anchoRej]` en `configurador.html`, con `anchoRej` sacado de `REJILLA_ANCHO_POR_VIGA[vigaIn]`.
