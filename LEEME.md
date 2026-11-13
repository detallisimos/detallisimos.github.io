# Detallísimos · detallisimos.com

## Qué hay en esta carpeta

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La página principal: portada, catálogo, qué se personaliza y contacto. |
| `modelos/*.js` | Un archivo por invitación (22). Se cargan solo cuando el visitante las ve, así la página abre rápido en el celular. |
| `CNAME` | Le dice a GitHub Pages que la página es `detallisimos.com`. No lo borres. |

## Lo primero que tienes que cambiar

Abre `index.html` con el Bloc de notas (o VS Code) y busca `CONFIGURACIÓN DE DETALLÍSIMOS`, casi al final:

```js
whatsapp:'50200000000',   // ← pon tu número: 502 + tus 8 dígitos, sin espacios ni +
facebook:'',              // ← link de tu página de Facebook (opcional)
instagram:''              // ← link de tu Instagram (opcional)
```

Todos los botones de WhatsApp de la página usan ese número.

## Cómo publicarla gratis en GitHub Pages

1. En GitHub crea un repositorio nuevo, por ejemplo `detallisimos` (público).
2. Toca **Add file → Upload files** y arrastra todo el contenido de esta carpeta (`index.html`, `CNAME`, `LEEME.md` y la carpeta `modelos`). Toca **Commit changes**.
3. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama **main**, carpeta **/ (root)** y guarda.
4. En la misma pantalla, en **Custom domain**, escribe `detallisimos.com` y guarda.
5. Donde compraste el dominio, entra a la configuración de **DNS** y agrega:

   | Tipo | Nombre | Valor |
   |---|---|---|
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | TU-USUARIO.github.io |

   Borra cualquier otro registro A o CNAME de `@` o `www` que ya venga puesto (los de "parking" del registrador).
6. Espera entre unos minutos y unas horas a que el DNS se actualice. Cuando GitHub muestre el visto bueno, marca **Enforce HTTPS**.

## Para actualizarla después

Sube de nuevo el archivo que cambiaste a ese mismo repositorio (**Add file → Upload files**). En uno o dos minutos ya se ve en detallisimos.com.
