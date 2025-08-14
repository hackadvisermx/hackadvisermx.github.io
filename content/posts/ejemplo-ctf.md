---
title: "[CTF] Buildooker 2 – Forensics Write-up (ejemplo)"
date: 2025-08-14
tags: ["forensics","ctf","privacy","flagmx"]
summary: "Recuperación de archivos borrados y análisis de metadatos."
draft: false
---

> **Nota**: Este es un post de ejemplo. Cámbialo por tu propio write-up.

## Contexto
Imagen ext4 con archivos borrados. Objetivo: recuperar `flagmx{}` y documentar metodología.

## Metodología
- `fls`/`icat` (The Sleuth Kit)
- Análisis de metadatos EXIF
- Hashing reproducible

## Pasos
```bash
# listar inodos borrados
fls -r -d image.raw > deleted.txt

# recuperar un inodo
icat image.raw 128-128-4 > suspect.jpg
```

## Hallazgos
- Se recuperó `suspect.jpg` con coordenadas en EXIF.
- Trazas de edición en `Artist` y `Software`.

## Lecciones aprendidas
- Documenta versiones y hashes.
- Automatiza extracción con un script.
- Mantén una cadena de custodia (incluso en CTF).

## Referencias
- https://www.sleuthkit.org/
