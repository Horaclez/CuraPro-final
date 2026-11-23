# CuraPro — Asistente de Curación Avanzada

Proyecto listo para compilar automáticamente en GitHub Actions:
- **Windows:** instalador tradicional (`CuraPro-Instalador.exe`) que instala la aplicación como **CuraPro** (`CuraPro.exe`) con acceso directo en el escritorio y menú Inicio.
- **Android:** paquete (`CuraPro.apk`) con ícono nativo y funcionamiento 100 % offline.

## Cómo subirlo a GitHub (una sola vez)
1. Crea un repositorio nuevo y vacío en GitHub.
2. Abre una terminal dentro de esta carpeta y ejecuta:
   ```bash
   git init
   git add .
   git commit -m "CuraPro v1.0"
   git branch -M main
   git remote add origin https://github.com/USUARIO/REPO.git
   git push -u origin main
   ```
3. Entra a la pestaña **Actions** o **Releases** en tu repositorio de GitHub para descargar `CuraPro-Instalador.exe` y `CuraPro.apk`.
