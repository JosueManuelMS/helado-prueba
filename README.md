# Blu — landing page (bosquejo inicial)

Landing page en Astro 5, Tailwind CSS 4, JavaScript y Cloudinary para **Blu: il gelato del barrio**.

## Desarrollo

```bash
npm install
npm run dev
```

## Cloudinary

1. Copia `.env.example` como `.env`.
2. Define `CLOUDINARY_CLOUD_NAME`.
3. Sube las fotos finales a Cloudinary con los public IDs indicados o cambia las variables `PUBLIC_CLOUDINARY_*`.

Mientras no exista configuración de Cloudinary, el bosquejo muestra fotografías remotas de referencia. Al configurar la cuenta, `CloudinaryImage.astro` usa el SDK oficial para entregar las imágenes desde Cloudinary con formato/calidad automáticos y recorte inteligente.

## Sveltia CMS

El panel editorial está disponible en `/admin/` una vez compilado. Durante el desarrollo con Astro se abre en `/admin/index.html`.

Sveltia edita `src/data/site.json`, donde están el SEO, enlaces, portada, sabores, historia, locales y llamada final.

Para entrar con GitHub:

1. Abre el panel y selecciona **Sign In with Token**.
2. Crea un token de acceso específico para `JosueManuelMS/helado-prueba`.
3. Concede `Contents: Read and write` y pega el token en Sveltia.

Los archivos subidos desde el panel se guardan en `public/uploads`. Para usar el selector nativo de Cloudinary dentro del CMS, agrega `media_libraries.cloudinary` en `public/admin/config.yml` con el `cloud_name` y el `api_key` públicos. Nunca agregues el API secret al repositorio.

## Contenido pendiente de validación

- Fotografías y logotipo oficiales de la marca.
- Sabores disponibles y precios.
- Direcciones, horarios y estado actual de cada sede.
- Enlaces finales de pedidos/delivery.
