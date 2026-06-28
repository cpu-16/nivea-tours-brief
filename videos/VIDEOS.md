# Videos — cómo usarlos en la web

> Videos **HD 1080p** sacados de los **originales de iPhone (4K)** y optimizados para web
> (H.264, 30fps, faststart, 4–11 MB c/u). **El conector de GitHub no importa binarios de video**,
> pero no hace falta: el repo es público y la web los **embebe por URL** desde el CDN **jsDelivr**
> (sirve `video/mp4` con rango → autoplay y seek). En `videos-posters/` hay un frame-póster JPG de
> cada uno (esos sí los importa el conector; úsalos como `poster=` / fallback).

⭐ = ideales para la portada (video de fondo autoplay + carrusel encima).

| Archivo | Contenido | URL embebible (jsDelivr) | Póster |
|---------|-----------|--------------------------|--------|
| `sunset-boat-ride.mp4` ⭐ | Atardecer desde el bote, mar abierto | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset-boat-ride.mp4) | `videos-posters/sunset-boat-ride.jpg` |
| `coiba-playa-isla.mp4` ⭐ | Playa de isla con agua turquesa y palmeras | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/coiba-playa-isla.mp4) | `videos-posters/coiba-playa-isla.jpg` |
| `agua-cristalina.mp4` ⭐ | Agua cristalina turquesa (snorkel/playa) | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/agua-cristalina.mp4) | `videos-posters/agua-cristalina.jpg` |
| `sunset-boat-ride-2.mp4` | Atardecer desde el bote (toma alterna) | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset-boat-ride-2.mp4) | `videos-posters/sunset-boat-ride-2.jpg` |
| `coiba-playa-bote.mp4` | Playa de isla con bote, agua cristalina | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/coiba-playa-bote.mp4) | `videos-posters/coiba-playa-bote.jpg` |
| `mirador-isla.mp4` | Vista de islote desde altura (mirador/senderismo) | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/mirador-isla.mp4) | `videos-posters/mirador-isla.jpg` |
| `paseo-en-bote.mp4` | Paseo en bote acercandose a un islote | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/paseo-en-bote.mp4) | `videos-posters/paseo-en-bote.jpg` |
| `fauna-monos.mp4` | Monos cariblancos en el bosque (fauna) | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/fauna-monos.mp4) | `videos-posters/fauna-monos.jpg` |
| `snorkel-arrecife.mp4` | Arrecife de coral con peces tropicales (snorkel) | [link](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/snorkel-arrecife.mp4) | `videos-posters/snorkel-arrecife.jpg` |

## Cómo embeberlos

```html
<!-- Portada: video de fondo autoplay silenciado, con poster de fallback -->
<video autoplay muted loop playsinline
       poster="videos-posters/sunset-boat-ride.jpg"
       src="https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset-boat-ride.mp4">
</video>
```

- **Portada:** uno de los ⭐ de fondo (`autoplay muted loop playsinline`) + carrusel de imágenes encima.
- **Sección de video dedicada:** el resto con `controls`, usando su `videos-posters/*.jpg` como `poster`.
- Patrón de URL: `https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/<archivo>`.
- Fallback si jsDelivr tarda en propagar un archivo nuevo: `https://github.com/cpu-16/nivea-tours-brief/raw/master/videos/<archivo>`.
