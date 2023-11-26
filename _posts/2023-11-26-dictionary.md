---
title: "Cómo restablecer tu diccionario personal en macOS como un experto"
date: 2023-11-26 15:26:00 -0600
categories: [tecnología, macOS]
tags: [macOS, terminal, diccionario, personalización]
---

# Restablecer el Diccionario Personal en macOS

En ocasiones, es posible que quieras **limpiar o editar tu diccionario personal** en macOS. Ya sea porque agregaste palabras por error o simplemente deseas comenzar de cero, macOS te permite gestionar fácilmente tu diccionario a través de los archivos que almacenan estas entradas.

## 🗂 Archivos Clave del Diccionario

macOS utiliza varios archivos para manejar tu diccionario personal, ubicados en `~/Library/Spelling/`:

- `dynamic-text.dat`: Almacena las palabras que agregas manualmente mientras trabajas.
- `LocalDictionary`: Contiene las palabras que han sido agregadas al diccionario a través de las preferencias del sistema o por aplicaciones.
- `dynamic-text-tmp.dat`: Es un archivo temporal que macOS utiliza para ciertas operaciones a nivel de sistema.

## 🧹 Borrando o Modificando el Diccionario

Puedes borrar palabras específicas o resetear completamente tu diccionario personal usando el Terminal.

### Eliminar Palabras Específicas

Para eliminar palabras específicas, puedes editar el archivo `LocalDictionary`:

```console
open -a TextEdit ~/Library/Spelling/LocalDictionary
```

Esto abrirá el archivo en TextEdit, donde puedes eliminar o añadir palabras.

### Restablecer el Diccionario Completo

Para eliminar todos los archivos y restablecer el diccionario:

```shell
rm ~/Library/Spelling/*
```

**Nota**: Debes cerrar todas las aplicaciones que puedan estar usando el diccionario para evitar posibles conflictos.

## 🔄 Recreación Automática de Archivos

Si eliminas estos archivos, macOS los recreará automáticamente la próxima vez que abras una aplicación que utilice el diccionario del sistema, como TextEdit o Pages.

## 🛠 Ejemplo Práctico

Si por ejemplo, deseas restablecer todo tu diccionario personal, simplemente abre Terminal y ejecuta:

```shell
rm ~/Library/Spelling/*
```

Luego, abre TextEdit y escribe algo para comprobar que el diccionario ha sido restablecido.

## 🎩 En Resumen

El manejo del diccionario personal en macOS es transparente y amigable. Ya sea para una limpieza rápida o una modificación meticulosa de las entradas, estas herramientas te otorgan el control total sobre las palabras que el sistema reconoce como correctas. ¡Experimenta y personaliza tu experiencia de escritura en macOS a tu gusto!