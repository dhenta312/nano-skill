# PILAR Design System (UII) — Referensi Token

Sumber resmi: **PILAR DESIGN SYSTEM UII** — file Figma `AYHhj3V2tSnZleViFsIjEx`
(https://www.figma.com/design/AYHhj3V2tSnZleViFsIjEx/PILAR-DESIGN-SYSTEM),
badge/token https://pilarng.github.io/badge.

Dokumen ini membundel pengetahuan PILAR agar skill `nano` self-contained — tidak
bergantung pada memory/skill di mesin tertentu.

## Token otoritatif (diekstrak dari audit "COLOR BALANCE EVALUATION")

### Palet teks

| Token | Nilai |
| --- | --- |
| primary | `#101828` |
| primary-2 | `#364153` |
| secondary | `#475569` |
| tertiary | `#64748B` |
| muted | `#94A3B8` |
| border | `#E5E7EB` |

Progression rekomendasi 11% → 32% → 45% → 67%, semua WCAG AA.

### Tipografi

- 10 / 12 / 14 px (Regular / Bold)

### Fokus

- `border/focus 2px offset 2`

### Konvensi nama CSS variable

- `--pilar-*` (mis. `--pilar-text-primary`)

## Yang masih hilang (belum bisa ditarik otoritatif)

File `AYHhj3V2...` adalah file **audit/dokumentasi**, bukan sumber token library. Nilai
berikut ada di library terbit `PILAR DESIGN SYSTEM` (libraryKey `lk-98ef97d7…`,
source: team) yang file sumbernya belum diberikan:

- Warna brand
- Warna semantik
- Skala spacing
- Shadow / elevation
- Radius

**Stopgap:** brand dipertahankan navy `#0044cd` (konsisten UII) sampai file sumber library
tersedia. Jika user memberi file sumber DS, tarik brand/spacing/shadow/radius dari sana dan
lengkapi theme `frontend/tailwind.config.js`.

## Cara terapkan

- Token Tailwind ada di `frontend/tailwind.config.js`.
- **Jangan** menulis hex langsung — kecuali pengecualian terdokumentasi.
- Konvensi pemakaian lengkap (nama token, aturan tombol disabled, label wajib, dll.) ada di
  `skills/dev-workflow/SKILL.md` bagian "Konvensi UI (PILAR)".
