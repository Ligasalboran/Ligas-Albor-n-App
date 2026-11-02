# Ligas Alborán · app Android

La carpeta `www` es la web completa (ya con tu URL y clave de Supabase). Con esta carpeta puedes:

## A) Sacar el APK en GitHub (sin instalar nada)
1. Crea una cuenta en github.com y un repositorio nuevo (puede ser privado).
2. Sube TODO el contenido de esta carpeta, incluida la carpeta oculta `.github` (si tu sistema la oculta, créala en GitHub con «Add file → Create new file» y el nombre `.github/workflows/apk.yml`).
3. Pestaña **Actions** → «Compilar APK» → **Run workflow**.
4. A los 5-10 minutos entra en la ejecución terminada y descarga el archivo **ligas-alboran-apk**; dentro está `app-debug.apk`.
5. Pásalo al móvil y ábrelo (Android pedirá permitir «instalar apps de origen desconocido»).

## B) Con PWABuilder
Sube la carpeta `www` a Netlify, Vercel o GitHub Pages, pega la dirección en pwabuilder.com y elige «Package for stores → Android».

## C) Con Android Studio
`npm install` · `npx cap add android` · `npx cap sync android` · `npx cap open android` → Build → Build APK(s).

## Notas
- Es un APK de pruebas (firmado con clave de depuración): sirve para instalarlo y compartirlo. Para Google Play hace falta uno firmado de lanzamiento.
- Cuando cambies `www/index.html`, vuelve a ejecutar el workflow (o `npx cap sync`) para generar un APK nuevo.
- La app necesita internet para leer los datos de Supabase.
- Para poner la web en internet sin APK, basta con subir el contenido de `www` a Netlify, Vercel o GitHub Pages.
