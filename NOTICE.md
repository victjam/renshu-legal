---
title: Third-party notices
permalink: /NOTICE
---

# Third-party notices

Forge ships or links against the work below. Each entry says what the work is,
where it lives in this repo, and under which terms it is used.

Required license notices are retained below. Asset provenance is documented
alongside its build pipeline; credits are also shown in Settings › Credits.

## Body diagram geometry — MuscleMap

`Forge/Resources/body-paths.json` is derived from
[**MuscleMap**](https://github.com/melihcolpan/MuscleMap) by Melih Colpan,
used under the **MIT License**.

MuscleMap ships its path data as Swift source rather than `.svg` files. The
paths were converted to a JSON resource and its sub-group shapes were dropped
(the exercise data resolves to whole muscles, so shading a sub-region would
imply a precision the data does not have). Nothing else about the artwork was
changed — all 159 path strings are byte-identical to the originals.

```
MIT License

Copyright (c) 2026 Melih Colpan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 3D muscle map — Blender Studio

`tools/anatomy/MuscleBody.usdz` is adapted from **Body Male - Realistic** by
**Julien Kaspar**, from Blender Studio's **Human Base Meshes v1.0.0** bundle,
released under **CC0**. Forge adapts the mesh into a neutral mannequin and marks
workout muscle regions on its surface.

See [the source record and generation steps](tools/anatomy/README.md) for the
official download, source checksum and modifications. The editable source
contains an embedded `SOURCE AND LICENSE.txt` record. The earlier Z-Anatomy
model is no longer used by this pipeline.

## Exercise data and media — ExerciseDB

Exercise names, muscles, equipment and instructions come from **ExerciseDB**
(`oss.exercisedb.dev` and its RapidAPI distribution). Its licence allows using
the dataset inside the product but not republishing it as an open API — which
is why `public.exercises` is readable only by `authenticated` users, never
`anon`, and why media is **hotlinked rather than copied** into our own
storage. See the note in
`supabase/migrations/20260824000001_r1_cuentas_y_rutinas.sql`.

## Swift packages

Linked via SwiftPM, not vendored into this repository. Each carries its own
licence:

- [SVGPath](https://github.com/nicklockwood/SVGPath) — Nick Lockwood
- [SDWebImageSwiftUI](https://github.com/SDWebImage/SDWebImageSwiftUI) — SDWebImage
- [supabase-swift](https://github.com/supabase/supabase-swift) — Supabase
