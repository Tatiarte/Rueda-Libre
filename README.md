
# Rueda Libre | Alquiler de bicicletas en Medellín

Sitio web de **Rueda Libre**, un negocio ficticio de alquiler de bicicletas, recorridos guiados y talleres básicos en Medellín. Es un ejercicio de la ruta básica de desarrollo de software en el que fui construyendo la misma marca con distintas herramientas: primero HTML y CSS, luego Bootstrap y, por último, Tailwind CSS.

## Ver la página

https://tatiarte.github.io/Rueda-Libre/

## Qué incluye

| Página | Archivo | Qué muestra |
| --- | --- | --- |
| Inicio | index.html | Portada, carrusel de destacados, rutas, servicios, flota de 7 bicicletas con precios, cómo alquilar y ubicación. |
| Tarifas | paginas/tarifas.html | Tablas de tarifas de alquiler y de recorridos guiados, más información importante. |
| Reservas | paginas/reservas.html | Formulario de reserva con validación nativa del navegador y horario de atención. |
| Rueda Nocturna | nocturna/index.html | Landing de la campaña de recorridos nocturnos (jueves a sábado, 7:30 p. m.) con rutas, planes, pasos e inscripción. Hecha con Tailwind. |
| Kit de componentes | nocturna/componentes.html | Botones, card de ruta, alertas y campos de formulario de la landing. |

## Tecnologías

- **HTML5:** estructura semántica (header, nav, main, section, article, footer), tablas, listas y formularios con validación nativa (required, minlength, pattern, min y max).
- **CSS3:** styles.css con Flexbox y CSS Grid, diseño **mobile first** e imágenes fluidas.
- **Bootstrap 5.3.9 (CDN):** navbar plegable y carrusel en el sitio principal. Se carga antes de styles.css para que los estilos propios tengan prioridad, y css/bootstrap-marca.css define las variables --bs-* con los colores y fuentes de la marca.
- **Tailwind CSS v4 (CLI):** la landing de Rueda Nocturna usa un tema propio definido con @theme en nocturna/src/input.css, que reemplaza la paleta genérica por la de la marca. Los botones se reutilizan con @apply y el modo oscuro se escribe con dark:.
- **JavaScript:** el de Bootstrap (navbar y carrusel) y un script corto en la landing que muestra el mensaje de inscripción exitosa.
- **Google Fonts:** Montserrat (títulos) y Open Sans (texto).
- **Git y GitHub:** control de versiones. Publicado con GitHub Pages.

### Paleta de la marca

| Color | Código |
| --- | --- |
| Crema | #FAF6EF |
| Azul Noche | #14213D |
| Gris Asfalto |#5B6470 |
| Verde Ruta | #1E7A4F |
| Naranja Pedal | #F39A2B |
| Amarillo Farol (campaña nocturna) | #FFD166 |

La  paleta y las fuentes son las mismas para Bootstrap y en Tailwind para que ambas partes del sitio se vean como una sola marca.

## Accesibilidad y responsive

- Atributo lang="es", texto alternativo en las imágenes y encabezados ordenados por jerarquía.
- Navegación con aria-label y encabezados ocultos visualmente (visually-hidden) para lectores de pantalla.
- Carrusel sin reproducción automática.
- Modo oscuro en la landing con prefers-color-scheme, con contraste revisado según WCAG 2.1 (mínimo 4,5:1; el valor más bajo medido fue 5,31:1).
- Estados de foco visibles para navegar con teclado.
- Enlaces externos con rel="noopener noreferrer".
- Revisado en anchos de 375 px, 768 px y 1280 px, sin desbordamiento horizontal.

## Estructura del proyecto

Rueda-Libre/
├── index.html                  # Inicio
├── Bitacora.txt                # Registro de resultados de los minirretos
├── css/
│   ├── styles.css              # Estilos propios del sitio
│   └── bootstrap-marca.css     # Tema de marca para Bootstrap
├── img/                        # Imágenes del sitio
├── paginas/
│   ├── tarifas.html
│   └── reservas.html
├── nocturna/                   # Landing con Tailwind
│   ├── index.html
│   ├── componentes.html
│   ├── prototipo.html          # Primer prototipo (Tailwind por CDN)
│   ├── package.json
│   └── src/
│       ├── input.css           # Tema y componentes de Tailwind
│       └── output.css          # CSS generado
└── pruebas/                    # Pruebas de Bootstrap
    ├── catalogo-bootstrap.html
    └── prueba-bootstrap.html




El CSS de nocturna/ se genera con el CLI de Tailwind. Desde esa carpeta:

bash
cd nocturna
npm install
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch

## Autora

Tatiana Hernández · [GitHub](https://github.com/Tatiarte)
