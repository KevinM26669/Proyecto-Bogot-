# Sitio web – Kevin Martínez · Concejo de Bogotá

Sitio estático (HTML + CSS). No necesita instalación, ni Node, ni React: se sube tal cual a cualquier hosting.

## Estructura

```
kevin-martinez-sitio/
├── index.html            ← la página completa
├── assets/
│   ├── css/styles.css    ← todos los estilos
│   └── img/              ← logo, foto, foto de Bogotá y logo de SUMA
├── vercel.json           ← configuración para Vercel
├── robots.txt
└── README.md
```

## Antes de publicar (pendientes)

1. **Enlace de la comunidad de WhatsApp.** Abre `index.html`, busca `href="#"` y reemplázalo por el enlace de invitación (empieza por `https://chat.whatsapp.com/`). Aparece en 4 lugares: pantalla de inicio, botón flotante, sección "Únete a la comunidad" y cierre "¡Súmate!".
2. **Formularios.** Abren el correo del visitante con los datos listos para enviar a `marcelo26101@outlook.es`. Si quieres que lleguen directo a una hoja de cálculo o al correo sin que el visitante abra su app, usa un servicio como Formspree o Netlify Forms y cambia el atributo `action` de cada `<form>`.
3. **Textos de la agenda.** La sección "Agenda de actividades" dice que pronto se publicarán fechas; edítala cuando tengas actividades.

## Publicar en Vercel (recomendado, gratis)

1. Crea una cuenta en https://vercel.com
2. Pulsa **Add New → Project**. Si no usas Git, instala Vercel CLI (`npm i -g vercel`) y ejecuta `vercel` dentro de esta carpeta. También puedes subir esta carpeta a un repositorio de GitHub y elegirlo en Vercel.
3. En la configuración elige **Framework Preset: Other**. No hay comando de build; el directorio de salida es la raíz (`./`).
4. Pulsa **Deploy**.

## Conectar tu dominio propio

1. Compra el dominio (GoDaddy, Namecheap, Hostinger, etc.).
2. En Vercel: **Project → Settings → Domains → Add** y escribe tu dominio.
3. Vercel te muestra los registros DNS que debes crear en tu proveedor de dominio (normalmente un registro `A` para la raíz y un `CNAME` para `www`). Pégalos allí.
4. Espera unos minutos u horas a que propague. El certificado HTTPS se genera solo.

## Otros hostings

- **Netlify / Cloudflare Pages:** arrastra la carpeta completa; no requieren configuración.
- **Hosting con cPanel (incluso uno con WordPress):** sube todo el contenido de la carpeta a `public_html` (o a una subcarpeta como `public_html/campana`) con el Administrador de archivos o FTP.

## Notas

- La fuente tipográfica (Montserrat y Satisfy) se carga desde Google Fonts; si no hay conexión usa Arial y una fuente cursiva del sistema.
- Para que al compartir el enlace aparezca una imagen de vista previa (WhatsApp, Facebook), agrega en el `<head>` una etiqueta `og:image` con la dirección completa de una imagen, por ejemplo `https://tudominio.com/assets/img/logo-km.jpg`.
