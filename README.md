# Portafolio — Yonder Maldonado Pabón

One-page portfolio construido con HTML, CSS y JavaScript puro (sin frameworks ni
dependencias de build). Responsive, con estructura semántica y sin imágenes
pesadas.

## Antes de publicar

Reemplaza estos valores de marcador en `index.html`:

- `tu-correo@ejemplo.com` → tu correo real
- `github.com/tu-usuario` → tu usuario de GitHub
- `linkedin.com/in/tu-usuario` → tu perfil de LinkedIn

## Estructura

```
portfolio/
├── index.html    # Contenido y estructura semántica
├── styles.css    # Estilos, tokens de diseño y responsive
├── script.js     # Menú móvil accesible
└── README.md
```

## Despliegue en GitHub Pages

1. Crea un repositorio en GitHub (por ejemplo `portafolio`).
2. Sube estos archivos a la rama `main`.
3. Ve a **Settings → Pages**.
4. En "Source", selecciona la rama `main` y la carpeta `/ (root)`.
5. Guarda. En un par de minutos tu sitio estará disponible en:
   `https://tu-usuario.github.io/portafolio/`

## Flujo de trabajo con Git (Git Flow simplificado)

Para un proyecto de este tamaño no necesitas el Git Flow completo (con
`develop`, `release`, etc.), pero sí puedes aplicar su idea central:

```
main            → siempre desplegable
feature/xxx     → una rama por cambio (ej: feature/seccion-contacto)
```

Ejemplo de flujo:

```bash
git checkout -b feature/ajustes-responsive
# ... haces cambios ...
git add .
git commit -m "fix: corrige el menú móvil en pantallas pequeñas"
git checkout main
git merge feature/ajustes-responsive
git push origin main
```

## Conventional Commits

Usa un prefijo que describa el tipo de cambio, seguido de una descripción
corta en minúscula y sin punto final:

| Prefijo    | Cuándo usarlo                                  |
|------------|-------------------------------------------------|
| `feat:`    | Agregas una funcionalidad o sección nueva        |
| `fix:`     | Corriges un error                                |
| `style:`   | Cambios de estilo que no afectan la lógica       |
| `docs:`    | Cambios en documentación (README, comentarios)   |
| `refactor:`| Reordenas código sin cambiar el comportamiento   |
| `chore:`   | Tareas de mantenimiento (configuración, assets)  |

Ejemplos:

```
feat: agrega sección de competencias
fix: corrige contraste de texto en modo móvil
docs: actualiza instrucciones de despliegue
chore: optimiza fuentes cargadas desde Google Fonts
```

Mantén cada commit enfocado en un solo cambio — evita mezclar varios tipos de
cambio en un mismo commit.
