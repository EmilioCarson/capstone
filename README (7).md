# Capstone TI2006B — Project Home

Repositorio del equipo para el Capstone de TI2006B. Aquí viven el código, los notebooks, la documentación de datos, los reportes y la evidencia de cada actividad.

Repositorio de referencia de la clase: <https://github.com/tec-research/ti2006b>

## Pregunta del proyecto

¿Qué tipos de Pokémon tienen las estadísticas base más altas en promedio, y existe relación entre el peso de un Pokémon y su total de estadísticas base?

## Audiencia

Compañeros del curso y el instructor que revisan el flujo de trabajo, así como cualquier persona que quiera entender un análisis de datos de nivel inicial dentro de un contexto inspirado en Pokémon GO.

## Fuente de datos

Tablas públicas de especies, tipos y estadísticas base del repositorio comunitario [`veekun/pokedex`](https://github.com/veekun/pokedex). El notebook las descarga cuando se ejecuta; no se suben datos crudos a este repositorio. Ver [`notebooks/README.md`](notebooks/README.md) y [`data/README.md`](data/README.md) para la procedencia completa.

## Resultado esperado

- Resumen de calidad de datos (columnas, valores faltantes).
- Gráficas interactivas en Plotly: distribución del total de estadísticas, ranking de los Pokémon más fuertes, conteo por tipo y relación peso vs. estadísticas.
- Conclusiones breves en [`reports/`](reports/).

## Limitación actual

Los datos describen especies y estadísticas de los juegos principales, **no** son telemetría de Pokémon GO: no incluyen cuentas, ubicaciones, encuentros, capturas ni batallas. Cualquier conclusión aplica a las especies, no al comportamiento de jugadores.

## How to start

```bash
git clone https://github.com/ORG/REPO.git
cd REPO
python3 -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
python -m pip install -r requirements.txt
jupyter lab notebooks/01-pokemon-go-analysis.ipynb
```

Ejecuta el notebook desde la raíz del repositorio. Necesita conexión a internet para descargar las tablas.

## Estructura

```text
.
├── .github/workflows/   # revisiones automáticas (ejecuta el notebook en cada push)
├── data/raw/            # datos fuente, solo cuando esté permitido
├── data/processed/      # tablas derivadas reproducibles
├── notebooks/           # notebooks exploratorios y notas de datos
├── src/                 # código Python reutilizable
├── reports/             # figuras y hallazgos
├── assignments/         # evidencia de actividades posteriores
├── requirements.txt
├── .gitignore
└── README.md
```

## Reglas del repositorio

- Un commit por cambio con sentido, con mensaje descriptivo.
- Nunca subir contraseñas, API keys, tokens, datos de estudiantes ni información de empresas.
- Las historias de usuario se validarán en Jira, ligadas al issue, commit o pull request correspondiente en GitHub.

## Reflexión

Lo que más dificultaría usar este repositorio a otro estudiante sería no saber qué pregunta responde, de dónde salen los datos o cómo ejecutar el notebook. Para evitarlo, el README explica la pregunta, la fuente y la limitación principal, e incluye los comandos exactos para empezar. Las carpetas siguen la estructura de la clase para que cada archivo tenga un lugar claro. Además, el `.gitignore` deja fuera los datos descargados y los archivos temporales, así que el repositorio se mantiene limpio y sin información sensible.
