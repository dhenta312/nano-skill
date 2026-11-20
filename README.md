# nano — AI Asisten Manajemen Proyek (Ide → Sistem → Dokumentasi)

Skill [Claude Code](https://claude.com/claude-code) untuk menjalankan siklus pengembangan
sistem secara utuh: **Diskusi & Analisis** (PRD/FSD/BPMN) → **Pengembangan Sistem**
(Figma PILAR + prototype Full Angular+Laravel atau Lite Vite) → **Dokumentasi**
(test report + user manual, dengan pilihan format Word/Excel/PowerPoint/PDF).

Repo ini **self-contained**: cukup clone, semua knowledge (termasuk PILAR design system
UII) sudah terbundel.

## Install

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/dhenta312/nano-skill.git ~/.claude/skills/nano
```

> Jika folder `~/.claude/skills/nano` sudah ada, hapus dulu: `rm -rf ~/.claude/skills/nano`.

## Cara pakai

- Ketik `nano` di Claude Code, atau sapa "hai nano".
- nano membaca `docs/nano/state.md` (per-proyek) untuk ingatan antar-sesi.

## Isi repo

```
nano/
├── SKILL.md                              # skill utama nano
├── README.md                             # file ini
├── references/
│   └── pilar-design-tokens.md            # token PILAR Design System UII
└── skills/
    └── dev-workflow/
        └── SKILL.md                      # konvensi dev UII (Laravel + Angular + PILAR)
```

## Aktifkan `dev-workflow` sebagai skill standalone (opsional)

`dev-workflow` dibundel sebagai referensi. Kalau ingin dipanggil sebagai skill tersendiri,
symlink ke lokasi skill:

```bash
ln -s ~/.claude/skills/nano/skills/dev-workflow ~/.claude/skills/dev-workflow
```

## Ketergantungan eksternal

- **Token PILAR** — sudah terbundel di `references/pilar-design-tokens.md` (palet teks,
  brand, semantik, spacing, radius, shadow). Bila ada token baru di file Figma PILAR,
  perbarui file tersebut.
- **Skill lain** yang dipanggil nano (instal terpisah bila perlu):
  `superpowers:*`, `ai-native-development-workflow`, `figma:*`, `generating-test-reports`,
  `screenshotting-web-app`, `editing-powerpoint-with-python`.
- **Document Skills (Anthropic)** — untuk output Word/Excel/PowerPoint/PDF di fase
  Dokumentasi:
  ```bash
  /plugin marketplace add anthropics/skills
  /plugin install document-skills@anthropic-agent-skills
  ```
  Dependensi Python: `python-docx` `openpyxl` `python-pptx` `pypdf` `pdfplumber`
  `reportlab` `pdf2image`.

## Update nano

```bash
cd ~/.claude/skills/nano
git pull
```

Untuk push update (butuh login): `gh auth login` lalu `git push`.
