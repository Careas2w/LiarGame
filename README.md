# Liar Game Online

Paquete listo para subir a GitHub Pages.

## Archivos
- `index.html` → la app web
- `supabase_setup.sql` → script para crear y actualizar tablas/policies en Supabase

## Lo único que tienes que hacer
1. En Supabase, abre `SQL Editor` → `New query`.
2. Pega `supabase_setup.sql` y pulsa `Run`.
3. En tu proyecto de Supabase, copia:
   - `Project URL`
   - `Publishable key` (o `anon key` si tu panel usa esa nomenclatura)
4. Abre `index.html`.
5. Busca estas líneas:
   - `const SUPABASE_URL = "PEGA_AQUI_TU_PROJECT_URL";`
   - `const SUPABASE_KEY = "PEGA_AQUI_TU_PUBLISHABLE_KEY_O_ANON_KEY";`
6. Sustitúyelas por tus datos.
7. Sube `index.html` a la raíz de tu repositorio de GitHub.
8. En GitHub: `Settings` → `Pages` → `Deploy from a branch` → rama `main` → carpeta `/(root)` → `Save`.

## Mejoras incluidas
- Mostrar y ocultar la clave de acceso.
- Ventana de unión ampliada a 6 minutos.
- Botón `Siguiente palabra` para crear otra ronda.
- Botón `Finalizar partida` que devuelve a la pantalla inicial de crear o unirse a sala.
- La palabra sale con la primera letra en mayúscula y con fuente más grande.

## Nota
La clave de acceso incluida en una web estática no es secreta de verdad. Sirve como barrera ligera, no como seguridad fuerte.


## Importante si ya tenías una versión anterior
Vuelve a ejecutar `supabase_setup.sql` en Supabase para asegurarte de que existe la columna `round_number`, necesaria para las rondas múltiples.
