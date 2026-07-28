# Sistema de diseño para infografías

Base reutilizable para todas las piezas del sitio. Un solo archivo
(`design-system.css`) + componentes en Quarto (`.qmd`) que se combinan
según la pieza.

## Paleta (Tableau 10 / ggthemes)

| Variable        | Color     | Uso sugerido                          |
|-----------------|-----------|----------------------------------------|
| `--t-blue`      | `#4E79A7` | Concepto A por defecto                 |
| `--t-orange`    | `#F28E2B` | Concepto B por defecto                 |
| `--t-red`       | `#E15759` | Alertas, contrastes fuertes            |
| `--t-teal`      | `#76B7B2` | Concepto secundario                    |
| `--t-green`     | `#59A14F` | Confirmación, "correcto"               |
| `--t-yellow`    | `#EDC948` | Resúmenes, síntesis                    |
| `--t-purple`    | `#B07AA1` | Ejemplos, analogías                    |
| `--t-pink`      | `#FF9DA7` | Acentos puntuales                      |
| `--t-brown`     | `#9C755F` | Notas, contexto                        |
| `--t-gray`      | `#BAB0AC` | Neutro / etiquetas                     |

Se eligió Tableau 10 porque es una paleta cualitativa probada,
legible y con buen contraste — pensada justo para distinguir
categorías con claridad, que es lo que buscás (didáctico y fácil
de leer). Blue/orange es además una combinación segura para
daltonismo, por eso es la pareja por defecto en comparaciones.

## Cómo usarlo en un `.qmd`

1. Agregá `design-system.css` al proyecto (referenciado en `_quarto.yml`
   con `format: html: css: design-system.css`, o por documento con
   `css: design-system.css` en el front matter).
2. Elegí un color de acento por concepto usando las clases
   `.accent-blue`, `.accent-orange`, `.accent-teal`, etc.
3. Armá la pieza combinando estos bloques:

### Título

```markdown
::: {.site-title}
[MÉTODOS]{} [VS]{.vs-divider} [METODOLOGÍA]{}
:::

::: {.subtitle-wrap}
::: {.subtitle-pill}
Entendiendo la diferencia
:::
:::
```

### Tarjeta de concepto (definición)

```markdown
::: {.concept-card .accent-blue}
### {{< fa bullseye >}} Concepto A

Texto de la definición.
:::
```

### Fila comparativa (tabla de diferencias)

Envolver todas las filas en un bloque que fija los dos colores una sola vez:

```markdown
::: {.compare-block style="--accent-a:var(--t-blue); --accent-b:var(--t-orange);"}

::: {.compare-row}
::: {.compare-left} Texto A :::
::: {.compare-label} ENFOQUE :::
::: {.compare-right} Texto B :::
:::

:::
```

### Callout / ejemplo

```markdown
::: {.callout .accent-purple}
Analogía o ejemplo aclaratorio.
:::
```

### Resumen final

```markdown
::: {.summary-callout .accent-yellow}
Idea final en una o dos líneas.
:::
```

## Por qué este sistema (y no calcar un diseño ajeno)

- Los **colores** son una paleta pública y estándar (Tableau/ggthemes),
  no la identidad de otra cuenta.
- La **composición visual** (tarjetas con barra de acento + ícono
  circular, filas de comparación con etiqueta central, callouts,
  resumen) es un lenguaje propio del sitio, consistente entre piezas.
- Cualquier infografía nueva se arma combinando los mismos bloques
  con distinto color de acento — así el sitio tiene identidad
  reconocible sin depender de replicar el layout de otra fuente cada vez.
