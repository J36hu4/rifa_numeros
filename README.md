# 🎉 Rifa de Números (00–99)

Página web sencilla para una rifa de 100 números, hecha para publicarse gratis en **GitHub Pages**.

- **Premio:** ₡100.000
- **Fecha:** Domingo 9 de agosto, junto con la Lotería Nacional
- **Costo del número:** ₡2.000
- **SINPE Móvil:** 6443-1669 · Jeshua Herrera Salas

## Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | Página principal que ve la gente (info + cuadrícula de números) |
| `admin.html` | Página de administración (solo se accede escribiendo la ruta en el navegador) |
| `numeros.json` | Aquí se guardan los números vendidos |
| `premio.jpg` | (Opcional) Foto del premio. Si la agregás con ese nombre, aparece en la página |

## Cómo publicarla en GitHub Pages

1. Creá un repositorio en [github.com/new](https://github.com/new) (por ejemplo `rifa-numeros`, **público**).
2. Subí estos archivos (desde esta carpeta):
   ```
   git remote add origin https://github.com/TU-USUARIO/rifa-numeros.git
   git push -u origin main
   ```
3. En el repositorio: **Settings → Pages → Branch: `main` → Save**.
4. En 1-2 minutos la página queda en:
   `https://TU-USUARIO.github.io/rifa-numeros/`

La página de administración queda en:
`https://TU-USUARIO.github.io/rifa-numeros/admin.html`
(no hay ningún enlace hacia ella, solo se llega escribiendo la ruta).

## Cómo marcar números vendidos

Entrá a `admin.html`, tocá un número, escribí el nombre del comprador (opcional) y guardá.

También podés:

- **🔎 Buscar quién compró un número:** escribí el número en la caja de búsqueda y te dice el comprador (o si está disponible).
- **☑️ Seleccionar varios:** activá el modo "Seleccionar varios", tocá todos los números que quiera la misma persona, escribí el nombre una sola vez y marcalos todos juntos (o liberalos juntos).

Hay dos formas de publicar los cambios:

### Opción A — Guardar directo desde la página (recomendada)
1. En GitHub: **Settings → Developer settings → Fine-grained personal access tokens → Generate new token**.
   - Repository access: **solo** tu repositorio de la rifa.
   - Permissions: **Contents → Read and write**.
2. En `admin.html`, botón **⚙️ Configurar GitHub**: poné tu usuario, el repo y el token (se guarda solo en tu navegador).
3. Después de marcar números, presioná **💾 Guardar en la página**. Listo.

### Opción B — Manual
Botón **⬇️ Descargar numeros.json** y reemplazá el archivo en el repositorio (en GitHub: abrí `numeros.json` → ✏️ Edit → pegá el contenido → Commit).

## Formato de numeros.json

```json
{
  "vendidos": {
    "07": "María Rodríguez",
    "23": ""
  }
}
```

La llave es el número (dos dígitos) y el valor es el nombre del comprador (puede ir vacío).
