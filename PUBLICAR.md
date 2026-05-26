# LEALA F1 World Championship — Cómo publicar en internet

Esta guía te lleva paso a paso para tener la web online y accesible desde
cualquier móvil, gratis, en unos 15 minutos.

═══════════════════════════════════════════════════════════════════════
   OPCIÓN RECOMENDADA: GITHUB PAGES (gratis, sin límite, sin caducidad)
═══════════════════════════════════════════════════════════════════════

## PASO 1 — Crear cuenta de GitHub (saltar si ya tienes)

1. Ve a https://github.com
2. Click en "Sign up" arriba a la derecha.
3. Sigue el proceso: usuario, email, contraseña.
4. Confirma el email.

(Anota tu nombre de usuario, lo necesitarás luego — ej: "juanperez".)

## PASO 2 — Crear un repositorio nuevo

1. Una vez dentro de GitHub, click en el "+" arriba a la derecha → "New repository".
2. **Repository name**: lo que quieras. Ejemplo: `leala-f1` o `mundial-2026`.
3. Marca **Public** (público). Es necesario para que GitHub Pages sea gratis.
4. NO marques "Add a README" ni nada más.
5. Click en "Create repository".

## PASO 3 — Subir los archivos del proyecto

GitHub te muestra una página vacía con instrucciones. Ignora todas y haz:

1. Click en "uploading an existing file" (link azul en el centro de la página).
2. Arrastra TODO el contenido de la carpeta del proyecto a la zona indicada:
   - index.html
   - css/ (con styles.css dentro)
   - js/ (con app.js dentro)
   - data/ (con data.json dentro)
   - assets/ (con todas tus imágenes)
   - README.md
   ⚠ IMPORTANTE: arrastra el CONTENIDO de la carpeta, no la carpeta entera.
3. Espera a que suban todos (puede tardar varios minutos si hay muchas
   imágenes en assets/).
4. Al final de la página, en "Commit changes": deja los textos por defecto
   y click en el botón verde "Commit changes".

## PASO 4 — Activar GitHub Pages

1. En la página del repositorio, arriba: pestaña "Settings".
2. En el menú izquierdo: "Pages".
3. En "Branch": selecciona "main" y deja "/(root)". Click "Save".
4. Espera 30-60 segundos.
5. Recarga la página. Verás un cuadro verde con la URL pública, algo como:
      https://TU-USUARIO.github.io/NOMBRE-REPO/
6. Esa es la URL que les pasas a tus amigos. Funciona ya en cualquier móvil.

## PASO 5 — Verificar

Abre la URL en el móvil. Deberías ver la portada directamente. Sin importar
ningún JSON. Las imágenes se cargan desde assets/, los datos desde
data/data.json automáticamente.

═══════════════════════════════════════════════════════════════════════
   ACTUALIZACIONES TRAS CADA CARRERA
═══════════════════════════════════════════════════════════════════════

Cuando termines de actualizar los resultados/sanciones/noticias en tu
ordenador (modo Admin), exporta el data.json limpio y súbelo:

1. En tu web local, ENTRA en modo admin (PIN).
2. Edita lo que toque: añade el resultado del GP, sanciones, noticias…
3. En el panel Admin pulsa "🧹 Exportar data.json limpio".
4. Eso te descarga un data.json nuevo (pesa ~30 KB).
5. Ve al repositorio de GitHub → click en la carpeta "data".
6. Click en el archivo "data.json".
7. Click en el icono del lápiz (arriba a la derecha) para editarlo.
   ALTERNATIVA: click en "Delete file" y luego "Add file > Upload"
   con el nuevo. Es más fácil si el contenido es totalmente distinto.
8. Pega el contenido del data.json nuevo (o sube el archivo).
9. Abajo "Commit changes".
10. En 30-60 segundos, todos verán los datos nuevos al recargar.

Para añadir imágenes nuevas (foto del último GP, una noticia, etc.):
1. En GitHub, navega a la carpeta correspondiente (ej. assets/photos/).
2. Click en "Add file" > "Upload files".
3. Arrastra los archivos nuevos (con el nombre correcto).
4. "Commit changes".

═══════════════════════════════════════════════════════════════════════
   SEGURIDAD — IMPORTANTE
═══════════════════════════════════════════════════════════════════════

Tus amigos verán la web pero pueden inspeccionar el código (F12 en el
navegador). El PIN de administrador está en data/data.json en claro.

⚠ ANTES DE PUBLICAR, cambia el PIN a uno fuerte que solo tú conozcas:

1. Abre data/data.json en un editor de texto.
2. Busca la línea:  "adminPin": "1234"
3. Cámbiala a algo como:  "adminPin": "f9k2-mx7q-vp4z"
   (Lo que quieras. Largo. Solo tú lo conoces.)
4. Guarda y súbelo a GitHub como en el paso de actualización.

Aun con esa precaución, debes saber que cualquiera con conocimientos
puede ver el contenido del data.json (incluido el PIN). Para mayor
seguridad real harían falta cambios al backend, que veremos más adelante.
Por ahora, esto basta para amigos.

═══════════════════════════════════════════════════════════════════════
   OPCIONALES — DOMINIO PROPIO
═══════════════════════════════════════════════════════════════════════

Si más adelante quieres que la web esté en algo como
"mundialleala.com" en vez de "tuusuario.github.io/leala-f1":

1. Compra un dominio (Namecheap, Cloudflare Registrar, IONOS…) ~10€/año.
2. En el repositorio: Settings > Pages > Custom domain > tu dominio.
3. Configura los DNS del dominio según las instrucciones de GitHub.
4. Esperas la propagación (~15 minutos a 24h).

═══════════════════════════════════════════════════════════════════════
   ALTERNATIVAS A GITHUB PAGES
═══════════════════════════════════════════════════════════════════════

- **Netlify** (https://netlify.com): Drag & drop de la carpeta. Aún más
  fácil que GitHub. URL tipo "leala-f1.netlify.app". También gratis.
- **Vercel** (https://vercel.com): Similar. Para webs estáticas
  con datos JSON, las tres son equivalentes.
- **Cloudflare Pages**: Otra alternativa gratis muy rápida.

Cualquiera de las cuatro vale. GitHub Pages tiene la ventaja de que
GitHub mismo es donde editas/versionas los datos.

═══════════════════════════════════════════════════════════════════════
   PROBLEMAS HABITUALES
═══════════════════════════════════════════════════════════════════════

**"Mis amigos abren la URL pero ven la portada sin datos"**
→ El data.json no se está cargando. Verifica que existe en data/data.json
  del repositorio y que tiene el formato correcto. Abre F12 en el navegador
  y mira la pestaña "Console". Si ves "No se encontró data/data.json" o
  algún error, dime y lo miramos.

**"Las imágenes no aparecen"**
→ Las imágenes deben estar EXACTAMENTE en assets/<carpeta>/<archivo>.webp
  con el nombre correcto. GitHub es case-sensitive: "Australia.webp" no
  es lo mismo que "australia.webp".

**"Veo la web vieja, no la actualización"**
→ Caché del navegador. Tus amigos deben hacer "recarga forzada":
  Ctrl+F5 (PC) o pull-to-refresh (móvil). Pasa una vez tras cada cambio.
