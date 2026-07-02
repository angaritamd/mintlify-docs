# Cómo editar la documentación de ClicRad

Bienvenido. Esta guía explica cómo actualizar `docs.clicrad.com` 
sin saber programar.

---

## Lo básico

La documentación vive en GitHub:
👉 https://github.com/angaritamd/mintlify-docs

Cada página es un archivo `.mdx` — es texto normal con algunos 
atajos de formato. Mintlify lo convierte automáticamente en la 
web bonita que ves en `docs.clicrad.com`.

**Cada vez que guardas un cambio en GitHub → la web se actualiza 
en 1-2 minutos. Automático.**

---

## Opción 1 — Editar directo en GitHub (más fácil)

1. Ve a https://github.com/angaritamd/mintlify-docs
2. Navega a la carpeta y archivo que quieres editar
   - Ejemplo: `coordinadores/generar-calendario.mdx`
3. Haz clic en el ícono de lápiz ✏️ (esquina superior derecha)
4. Edita el texto
5. Al terminar, baja hasta "Commit changes"
6. Escribe una nota breve: _"Actualicé instrucciones del calendario"_
7. Clic en **Commit changes**
8. Listo — en 2 minutos se ve en `docs.clicrad.com`

---

## Opción 2 — Editar con Claude vía Slack

Si conectaste el agente de Mintlify a Slack, puedes escribir 
en el canal correspondiente:

> "Actualiza la página de permutas para agregar que el coordinador 
> puede rechazar con un comentario"

El agente hace el cambio automáticamente.

---

## Estructura de carpetas


---

## Formato básico de un archivo .mdx

```mdx
---
title: "Título de la página"
description: "Descripción corta"
---

Texto normal aquí. Puedes escribir como en Word.

## Subtítulo

Más texto...

## Otro subtítulo

- Item de lista
- Otro item
```

---

## Componentes especiales (copiar y pegar)

**Nota informativa:**
```mdx
<Note>
  Esto es una nota importante para el usuario.
</Note>
```

**Advertencia:**
```mdx
<Warning>
  Cuidado con esto antes de continuar.
</Warning>
```

**Tip útil:**
```mdx
<Tip>
  Consejo práctico para el usuario.
</Tip>
```

**Pasos numerados:**
```mdx
<Steps>
  <Step title="Primer paso">
    Descripción de qué hacer.
  </Step>
  <Step title="Segundo paso">
    Descripción de qué hacer.
  </Step>
</Steps>
```

**Cards de navegación:**
```mdx
<Card title="Ir a esta sección" icon="arrow-right" href="/ruta/pagina">
  Descripción corta de a dónde lleva.
</Card>
```

**Pestañas:**
```mdx
<Tabs>
  <Tab title="Opción A">
    Contenido de la opción A.
  </Tab>
  <Tab title="Opción B">
    Contenido de la opción B.
  </Tab>
</Tabs>
```

---

## Agregar una página nueva

1. Crea un archivo `.mdx` en la carpeta correcta
   - Ejemplo: `coordinadores/nueva-funcion.mdx`
2. Añade el encabezado:
```mdx
---
title: "Nombre de la página"
description: "Descripción corta"
---
```
3. Abre `docs.json` y agrega la ruta en la sección correcta:
```json
"coordinadores/nueva-funcion"
```
4. Commit y listo.

---

## ¿Necesitas imágenes o screenshots?

Mintlify soporta imágenes. Para agregar una:

1. Sube la imagen a la carpeta `/images/` del repo
2. En el archivo `.mdx` escribe:
```mdx
![Descripción de la imagen](/images/nombre-archivo.png)
```

---

## Contacto

¿Dudas sobre la documentación?
📧 emails@clicrad.com
