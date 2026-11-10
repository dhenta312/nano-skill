# nano — AI Asisten Manajemen Proyek (Ide → Dokumentasi)

Skill [Claude Code](https://claude.com/claude-code) untuk menjalankan siklus pengembangan
sistem secara utuh: **Diskusi & Analisis** (PRD/FSD/BPMN) → **Pengembangan Sistem**
(Figma PILAR + prototype Angular+Laravel) → **Dokumentasi** (test report + user manual).

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

## Ketergantungan eksternal (belum terbundel)

- **File sumber library PILAR** — nilai brand, spacing, shadow, radius belum tersedia;
  lihat `references/pilar-design-tokens.md` untuk detail & stopgap.
- **Skill lain** yang dipanggil nano (instal terpisah bila perlu):
  `superpowers:*`, `ai-native-development-workflow`, `figma:*`, `generating-test-reports`,
  `screenshotting-web-app`, `editing-powerpoint-with-python`.

## Update nano

```bash
cd ~/.claude/skills/nano
git pull
```

Untuk push update (butuh login): `gh auth login` lalu `git push`.
