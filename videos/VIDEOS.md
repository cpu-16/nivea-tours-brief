# Videos — cómo usarlos en la web

> **El conector de GitHub no importa binarios de video, solo imágenes/texto.**
> No hace falta importarlos: el repo es **público**, así que la web los **embebe por URL**
> desde el CDN **jsDelivr** (sirve `video/mp4` con soporte de rango → autoplay y seek funcionan).
> Para que la IA igual "vea" cada video, en `videos-posters/` hay un **frame-póster JPG** de cada uno
> (esos sí los importa el conector y sirven de `poster=` / fallback del autoplay).

## URLs listas para `<video src>`

⭐ = ideales para la portada (según el brief: video de fondo en autoplay + carrusel encima).

| Archivo | URL embebible (jsDelivr) | Póster (imagen) |
|---------|--------------------------|-----------------|
| `animales.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/animales.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/animales.mp4) | `videos-posters/animales.jpg` |
| `animales2.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/animales2.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/animales2.mp4) | `videos-posters/animales2.jpg` |
| `animales3.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/animales3.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/animales3.mp4) | `videos-posters/animales3.jpg` |
| `cebaco.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/cebaco.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/cebaco.mp4) | `videos-posters/cebaco.jpg` |
| `cebaco2.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/cebaco2.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/cebaco2.mp4) | `videos-posters/cebaco2.jpg` |
| `coiba.mp4` ⭐ | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/coiba.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/coiba.mp4) | `videos-posters/coiba.jpg` |
| `coiba2.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/coiba2.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/coiba2.mp4) | `videos-posters/coiba2.jpg` |
| `playa azul.mp4` ⭐ | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/playa%20azul.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/playa%20azul.mp4) | `videos-posters/playa azul.jpg` |
| `senderismo.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/senderismo.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/senderismo.mp4) | `videos-posters/senderismo.jpg` |
| `sunset boat ride.mp4` ⭐ | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset%20boat%20ride.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset%20boat%20ride.mp4) | `videos-posters/sunset boat ride.jpg` |
| `sunset.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset.mp4) | `videos-posters/sunset.jpg` |
| `sunset2.mp4` | [https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset2.mp4](https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset2.mp4) | `videos-posters/sunset2.jpg` |

## Cómo embeberlos

```html
<!-- Portada: video de fondo autoplay silenciado, con poster como fallback -->
<video autoplay muted loop playsinline
       poster="videos-posters/sunset boat ride.jpg"
       src="https://cdn.jsdelivr.net/gh/cpu-16/nivea-tours-brief@master/videos/sunset%20boat%20ride.mp4">
</video>
```

- **Portada:** uno de los ⭐ como fondo (`autoplay muted loop playsinline`) + carrusel de imágenes encima.
- **Sección de video dedicada:** el resto con `controls`, usando su `videos-posters/*.jpg` como `poster`.
- Si jsDelivr tarda en propagar un archivo nuevo, fallback: `https://github.com/cpu-16/nivea-tours-brief/raw/master/videos/<archivo>`.
