# cifrato-email-assets

Las imágenes de los correos de Cifrato. **Es público a propósito**: los clientes
de correo no pueden pedir imágenes detrás de autenticación, así que tienen que
estar en una URL abierta.

No pongas nada aquí que no quieras que vea cualquiera.

## Cómo se sirven

Por jsDelivr, **fijadas al commit**:

```
https://cdn.jsdelivr.net/gh/carlespinosa11/cifrato-email-assets@<hash>/<carpeta>/<archivo>
```

El `@<hash>` no es opcional. Con `@master`, jsDelivr responde 404 o sirve caché
vieja justo después de hacer push, que es cuando uno está probando el correo y
cree que la imagen está mal.

## Cómo se organiza

Una carpeta por correo o campaña (`email-primer-ano`, `hotsale-2026-10`,
`invitacion-premium`, `email5-webinar-en-vivo`...), más `assets/` para lo que se
reutiliza entre varios.

Al armar un correo nuevo, carpeta nueva. No se reaprovechan carpetas viejas:
cambiarle una imagen a una carpeta le cambia la imagen a los correos que ya
salieron y que la gente todavía puede abrir.

## Reglas de las imágenes

- **Al doble del tamaño en que se muestran** (1200 px de ancho para mostrar a
  600) y con `width` y `height` fijos en el `<img>`.
- **`alt` siempre**, con el mensaje clave: muchos clientes bloquean imágenes por
  defecto y el `alt` es lo único que queda.
- **Los GIF, por debajo de 2 MB.** Uno de 4,4 MB tarda en celular. Para previews
  y reportes se usa una versión estática, porque una captura del GIF a mitad de
  animación sale borrosa.

Las reglas completas de maquetación están en la skill de envío de correo, en
`skills/envio-email/referencia/plantillas.md` dentro de
[`cifrato-dashboard`](https://github.com/carlespinosa11/cifrato-dashboard).
