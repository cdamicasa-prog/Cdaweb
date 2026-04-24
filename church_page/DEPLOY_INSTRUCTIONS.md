# 🚀 Subir la página a GitHub SIN instalar Git (todo desde el navegador)

---

## Paso 1: Crear cuenta de GitHub — 🌐 EN EL NAVEGADOR

1. Ve a **https://github.com** y crea una cuenta (o inicia sesión si ya tienes)

---

## Paso 2: Crear un repositorio — 🌐 EN EL NAVEGADOR

1. Ve a **https://github.com/new**
2. Configura:
   - **Repository name:** `cdamicasa-website`
   - **Description:** `Página web Iglesia CDA Mi Casa`
   - ✅ **SÍ marca** "Add a README file" (esto crea el repo listo para subir archivos)
3. Haz clic en **"Create repository"**

---

## Paso 3: Subir los archivos — 🌐 EN EL NAVEGADOR

1. En tu repositorio recién creado, haz clic en el botón **"Add file"** → **"Upload files"**
2. Abre el **Explorador de archivos** de Windows y navega a:
   ```
   d:\03. Diseño\OneDrive - Iglesia Cristiana CDA Internacional\Página Web CdaMiCasa\church_page\dist\
   ```
3. **Selecciona TODOS los archivos y carpetas** dentro de `dist` (Ctrl+A) y **arrástralos** a la zona de carga de GitHub
4. Espera a que todos se carguen (verás una barra de progreso)
5. En "Commit changes" escribe: `Página web CdaMiCasa - versión inicial`
6. Haz clic en **"Commit changes"**

> ⚠️ **IMPORTANTE:** GitHub no permite subir carpetas vacías ni más de 100 archivos a la vez por la interfaz web.
> Si te da error, sube las carpetas de una en una:
> - Primero sube `index.html`, `staticwebapp.config.json`
> - Luego crea la carpeta `css` (Add file → Create new file → escribe `css/style.css`) y pega el contenido
> - Luego repite con cada carpeta de `assets`

### Método alternativo para subir carpetas:

Si arrastrar no funciona bien, puedes crear archivos uno a uno:

1. Haz clic en **"Add file"** → **"Create new file"**
2. En el nombre escribe la ruta completa, por ejemplo: `css/style.css`
   (GitHub creará la carpeta `css` automáticamente)
3. Pega el contenido del archivo
4. Haz clic en **"Commit changes"**
5. Repite para cada archivo

---

## Paso 4: Verificar — 🌐 EN EL NAVEGADOR

Tu repositorio debería verse así:

```
cdamicasa-website/
├── README.md
├── index.html
├── staticwebapp.config.json
├── css/
│   └── style.css
└── assets/
    ├── fonts/
    ├── reuniones/
    ├── Reuniones vertical/
    ├── medios de pago/
    ├── cdamicasa-blanco.png
    ├── pastores_transparente_opt.png
    └── ...
```

---

## Paso 5: Conectar con Azure Static Web Apps — 🌐 EN AZURE (NAVEGADOR)

1. Ve a **https://portal.azure.com**
2. Busca **"Static Web Apps"** → clic en **"+ Crear"**
3. Configura:
   - **Grupo de recursos:** Crea nuevo (ej: `rg-cdamicasa`)
   - **Nombre:** `cdamicasa`
   - **Plan:** `Gratuito (Free)`
   - **Región:** `East US 2`
   - **Origen:** `GitHub`
4. **Inicia sesión con GitHub** y selecciona:
   - **Repositorio:** `cdamicasa-website`
   - **Rama:** `main`
5. **Detalles de compilación:**
   - **Preajuste:** `Custom`
   - **Ubicación de la aplicación:** `/`
   - **API y resultado:** _(dejar vacío)_
6. Clic en **"Revisar y crear"** → **"Crear"**

---

## Paso 6: ¡Tu página está en línea! — 🌐 EN AZURE (NAVEGADOR)

1. Espera 2-3 minutos
2. En tu Static Web App verás una URL como:
   ```
   https://nombre-aleatorio.azurestaticapps.net
   ```
3. ¡Ábrela y disfruta tu página! 🎉

---

## 📝 Para futuras actualizaciones (sin Git)

1. Ve a tu repositorio en GitHub
2. Navega al archivo que quieras actualizar (ej: `index.html`)
3. Haz clic en el ícono del **lápiz ✏️** para editarlo
4. Haz los cambios y clic en **"Commit changes"**
5. Azure desplegará automáticamente los cambios
