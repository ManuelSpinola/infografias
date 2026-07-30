# Roadmap — Conservación de la Biodiversidad

Banco de ideas para la futura sección "Conservación de la Biodiversidad" del sitio de infografías. Marca cada casilla conforme vayas completando el `.qmd` correspondiente.

> Nota: los nombres de archivo son sugerencias siguiendo la convención `snake_case.qmd` ya usada en el sitio (ej. `metodo_vs_metodologia.qmd`). Ajusta si prefieres otro nombre.

## Conceptos fundamentales

- [x] Conservación biológica: qué es y qué no es — `conservacion_biologica_definicion.qmd`
- [x] Niveles de biodiversidad: genética, de especies, de ecosistemas — `niveles_biodiversidad.qmd`
- [ ] Especies indicadoras vs. paraguas vs. bandera vs. clave — `especies_indicadoras_paraguas_bandera_clave.qmd`
- [ ] Conservación in situ vs. ex situ — `conservacion_in_situ_vs_ex_situ.qmd`

## Genética de la conservación

- [x] Diversidad genética y viabilidad poblacional — `diversidad_genetica_viabilidad.qmd`
- [ ] Cuello de botella genético vs. efecto fundador — `cuello_botella_vs_efecto_fundador.qmd`
- [ ] Depresión endogámica y tamaño efectivo poblacional (Ne vs. N censal) — `ne_vs_n_censal.qmd`
- [ ] Flujo génico y conectividad genética — `flujo_genico_conectividad.qmd`

## Conectividad y paisaje

- [x] Corredores biológicos: conectividad estructural vs. funcional — `corredores_biologicos_conectividad.qmd`
- [ ] Fragmentación del hábitat vs. pérdida de hábitat — `fragmentacion_vs_perdida_habitat.qmd`
- [ ] Metapoblaciones: parches, dispersión, dinámica de extinción-recolonización — `metapoblaciones.qmd`
- [ ] Efecto de borde — `efecto_de_borde.qmd`

## Amenazas y viabilidad poblacional

- [ ] Análisis de viabilidad poblacional (PVA) y tamaño mínimo viable — `pva_tamano_minimo_viable.qmd`
- [ ] Especie exótica vs. especie invasora — `exotica_vs_invasora.qmd`
- [ ] Extirpación (extinción local) vs. extinción funcional vs. extinción global — `extirpacion_vs_extincion.qmd`

## Instrumentos y estrategias de conservación

- [ ] Categorías de áreas protegidas (UICN) — `categorias_areas_protegidas_uicn.qmd`
- [ ] Hotspots de biodiversidad y priorización espacial — `hotspots_biodiversidad.qmd`
- [ ] Servicios ecosistémicos como argumento de conservación — `servicios_ecosistemicos.qmd`

---

## Para cuando se lance la sección

Snippet para agregar en `_quarto.yml` (sidebar), ajustando la lista de `contents` según lo que ya esté terminado:

```yaml
      - section: "Conservación de la biodiversidad"
        contents:
          - text: "Conservación biológica: qué es y qué no es"
            href: infografias/conservacion_biologica_definicion.qmd
          # ... agregar el resto conforme se completen
```

## Notas

- Total de ideas: 18. Las otras secciones del sitio arrancaron con 2–7 infografías, así que no hace falta completar todo el banco antes de lanzar — basta un primer lote pequeño.
- Cuando quieras, se puede priorizar un primer lote de 6–8 para lanzar la sección.
