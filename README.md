# CuraPro CL — Asistente de Curación Avanzada

Este repositorio genera automáticamente, con GitHub Actions:
1. **APK de Android** (`CuraPro-CL.apk`)
2. **Instalador de Windows** (`CuraPro-CL-Setup-<versión>.exe`)

## Pasos
1. Crea un repositorio nuevo en GitHub y sube todo el contenido de esta carpeta.
2. **Archivos ocultos (importante):** el explorador y la web de GitHub a veces no suben los que empiezan con punto. Revisa que existan en el repo:
   - `.github/workflows/build.yml`
   - `.gitignore`
   Si faltan, en GitHub usa **Add file → Create new file**, escribe el nombre (por ejemplo `.github/workflows/build.yml`; al escribir las barras se crean las carpetas) y pega el contenido de `PARA_COPIAR/build.yml.txt` y `PARA_COPIAR/gitignore.txt`.
3. Ve a la pestaña **Actions → Build CuraPro CL → Run workflow** (también corre solo al hacer push a `main`). Tarda entre 10 y 20 minutos.
4. Al terminar, entra a la ejecución y descarga los **Artifacts**: `CuraPro-CL-APK` y `CuraPro-CL-Windows`.
5. Para publicarlos en **Releases**: crea una etiqueta `v2.0.0` (Releases → Draft a new release → Choose a tag → crear `v2.0.0`). El workflow adjunta ambos archivos.

## Notas
- El APK es de **depuración** (firmado con clave de depuración): se instala activando "orígenes desconocidos". Para Play Store hay que firmar una versión release.
- Windows puede mostrar un aviso de SmartScreen porque el instalador no está firmado: "Más información → Ejecutar de todas formas".
- En el APK, "Imprimir/PDF" y la descarga de Word pueden no funcionar (limitación del WebView de Android); en Windows sí.
- Los datos (seguimiento, fotos, inventario, borrador) se guardan solo en el dispositivo. No ingreses datos que identifiquen al paciente sin cumplir la normativa de tu institución.
- Herramienta de apoyo: no reemplaza el juicio clínico. Valida reglas, insumos y escalas con los protocolos vigentes.
