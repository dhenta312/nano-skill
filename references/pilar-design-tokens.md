# PILAR Design System (UII) — Referensi Token

Sumber resmi: **PILAR DESIGN SYSTEM UII** — file Figma `AYHhj3V2tSnZleViFsIjEx`
(https://www.figma.com/design/AYHhj3V2tSnZleViFsIjEx/PILAR-DESIGN-SYSTEM),
badge/token https://pilarng.github.io/badge.

Library terbit: **PILAR DESIGN SYSTEM** (libraryKey `lk-98ef97d7…`, source: team).

Dokumen ini membundel pengetahuan PILAR agar skill `nano` self-contained. Nilai di bawah
diekstrak langsung dari file Figma di atas (variabel lokal + effect styles), lengkap.

## Koleksi variabel

| Koleksi | Isi | Mode |
| --- | --- | --- |
| `primitive` | warna dasar (brand, semantik) | Value |
| `role` | peran semantik | Light |
| `purpose` | token terpakai (`text/*`, `background/*`, `border/*`, `icon/*`) | Light |
| `responsive` | spacing, radius, paragraph spacing | Desktop/Tablet/Mobile |
| `language` | string (mis. `feedback/success`) | Indonesia/English |

## Teks

| Token | Nilai |
| --- | --- |
| primary | `#101828` |
| primary-2 | `#364153` |
| secondary | `#475569` |
| tertiary | `#64748B` |
| muted | `#94A3B8` |
| border | `#E5E7EB` |

## Tipografi

- 10 / 12 / 14 px (Regular / Bold).

## Brand (2 skala)

### brand1 — biru navy

| Step | Nilai |
| --- | --- |
| 50 | `#E5EEFF` |
| 100 | `#CCDDFF` |
| 200 | `#99BBFF` |
| 300 | `#6699FF` |
| 400 | `#3377FF` |
| 500 | `#0055FF` |
| 600 | `#0044CD` |
| 700 | `#003399` |
| 800 | `#002266` |
| 900 | `#001133` |
| 950 | `#00081A` |

### brand2 — kuning

| Step | Nilai |
| --- | --- |
| 50 | `#FFFEEB` |
| 100 | `#FFFCD1` |
| 200 | `#FFF9A8` |
| 300 | `#FFF67A` |
| 400 | `#FFF34D` |
| 500 | `#FFF023` |
| 600 | `#F5E400` |
| 700 | `#B8AB00` |
| 800 | `#7A7200` |
| 900 | `#3D3900` |
| 950 | `#1F1C00` |

## Warna semantik

### success
50 `#F0FDF4` · 100 `#DCFCE7` · 200 `#B9F8CF` · 300 `#7BF1A8` · 400 `#05DF72` · 500 `#00C950` ·
600 `#00A63E` · 700 `#008236` · 800 `#016630` · 900 `#0D542B` · 950 `#032E15`

### warning
50 `#FFFBEB` · 100 `#FEF3C6` · 200 `#FEE685` · 300 `#FFD230` · 400 `#FFB900` · 500 `#FE9A00` ·
600 `#E17100` · 700 `#BB4D00` · 800 `#973C00` · 900 `#7B3306` · 950 `#461901`

### destructive
50 `#FEF2F2` · 100 `#FFE2E2` · 200 `#FFC9C9` · 300 `#FFA2A2` · 400 `#FF6467` · 500 `#FB2C36` ·
600 `#E7000B` · 700 `#C10007` · 800 `#9F0712` · 900 `#82181A` · 950 `#460809`

### information
50 `#EFF6FF` · 100 `#DBEAFE` · 200 `#BEDBFF` · 300 `#8EC5FF` · 400 `#51A2FF` · 500 `#2B7FFF` ·
600 `#155DFC` · 700 `#1447E6` · 800 `#193CB8` · 900 `#1C398E` · 950 `#162456`

## Spacing (px)

`-50=-2` · `0=0` · `25=1` · `50=2` · `100=4` · `150=6` · `200=8` · `250=10` · `300=12` ·
`350=14` · `400=16` · `500=20` · `600=24` · `700=28` · `800=32` · `900=36` · `1000=40` ·
`1100=48` · `1200=56` · `1300=64` · `1400=72` · `1500=80`

## Radius (px)

`none=0` · `xxxs=2` · `xxs=4` · `xs=6` · `s=8` · `m=10` · `l=12` · `xl=14` · `xxl=16` ·
`xxxl=20` · `full=9999`

## Shadow / elevation (effect styles)

| Nama | Efek |
| --- | --- |
| `xs` | drop `y=1 blur=2` `#000` 5% |
| `s` | drop `y=1 blur=2` 6% + drop `y=1 blur=3` 10% |
| `m` | drop `y=2 blur=4 spread=-1` 6% + drop `y=4 blur=6 spread=-1` 10% |
| `l` | drop `y=4 blur=6 spread=-2` 5% + drop `y=10 blur=15 spread=-3` 10% |
| `xl` | drop `y=10 blur=10 spread=-5` 4% + drop `y=20 blur=25 spread=-5` 10% |
| `xxl` | drop `y=25 blur=50 spread=-12` 25% |
| `inner` | inner `y=2 blur=4` `#000` 6% |
| `focus` | drop `spread=4` `#0044CD` + drop `spread=2` `#0044CD` (ring fokus) |

## Konvensi nama CSS variable

- `--pilar-*` (mis. `--pilar-text-primary`).

## Cara terapkan

- Token Tailwind ada di `frontend/tailwind.config.js`.
- **Jangan** menulis hex langsung — kecuali pengecualian terdokumentasi.
- Konvensi pemakaian lengkap (nama token, aturan tombol disabled, label wajib, dll.) ada di
  `skills/dev-workflow/SKILL.md` bagian "Konvensi UI (PILAR)".
