# AuraPath Brand Assets

Public image assets for AuraPath AI: the logo, marks, LinkedIn banner, favicons,
team headshots, and ready-to-use email signatures. This repository is **public
on purpose** because email and web clients need to fetch these images from a
stable public URL.

Brand line: *Impactful AI, at scale.* Palette: obsidian `#000000`, bone
`#F0EBE5`, gilt `#C7B68A`, gold / aurum `#B8923D`, warm ink `#1F1E1D`, muted
`#6B6862`.

## ⚠️ The root files are live, do not move them

Three files at the repository root are referenced by URL inside live email
signatures. **Do not rename, delete, move, or make this repo private**, or every
installed signature breaks.

| File | What it is | Linked from |
| --- | --- | --- |
| `logo.png` | Gold AuraPath monogram, 128px, transparent | every signature |
| `headshot.png` | Brandon Slicklein, circular, gold ring, 128px | Brandon's signature |
| `travis-headshot.png` | Travis Johnson, circular, gold ring, 128px | Travis's signature |

Raw URL pattern (this is what the signatures use):

```
https://raw.githubusercontent.com/Aurapath/brand-assets/main/<file>
```

## `branding/` — the full asset set

Everything produced for the AuraPath brand kit. The working copies also live on
Brandon's machine at `~/Desktop/AuraPath Branding/`.

### Logo and marks
| File | Use |
| --- | --- |
| `aurapath-mark-gold-transparent.png` | Gold monogram on transparent. Light or dark backgrounds. |
| `aurapath-mark-white-transparent.png` | White / bone monogram on transparent. Dark backgrounds. |
| `aurapath-mark-white-transparent-512.png` | Same, padded to a 512px square. |

### LinkedIn banner
| File | Use |
| --- | --- |
| `aurapath-linkedin-cover.png` | Personal cover banner, 1584×396 rendered at 2× (3168×792). Content sits in the upper-center safe zone so LinkedIn's crop never clips it. |
| `aurapath-linkedin-cover.html` | Editable source for the banner. |

### Favicons and app icon
| File | Use |
| --- | --- |
| `aurapath-favicon.ico` | Multi-size icon (16 → 256) for drop-in `favicon.ico`. |
| `aurapath-favicon-1024.png` | App-icon master. |
| `aurapath-favicon-512.png` / `-180.png` / `-32.png` / `-16.png` | Web and Apple-touch sizes. |
| `aurapath-favicon.html` | Editable source (white monogram on the dark glow background). |

### Headshots
Circular, with a thin brand-gold ring, 320px masters. The 128px web copies used
by signatures live at the repo root.
| File | Person |
| --- | --- |
| `aurapath-headshot-circle.png` | Brandon Slicklein |
| `aurapath-travis-circle.png` | Travis Johnson |

### Email signatures
Self-contained, Gmail-ready HTML. Open the file, select all, copy, and paste
into Gmail (**⚙ Settings → Signature**). Images load from the root URLs above, so
the signature stays under Gmail's size limit.
| File | Person |
| --- | --- |
| `aurapath-email-signature.html` | Brandon Slicklein |
| `aurapath-email-signature-travis.html` | Travis Johnson |
| `aurapath-email-signature-preview.png` | Brandon's rendered preview |
| `aurapath-email-signature-travis-preview.png` | Travis's rendered preview |

## Generating a new signature

Use the **`aurapath-signature`** Claude Code skill in
[`Aurapath/skills_directory`](https://github.com/Aurapath/skills_directory). Give
it a name, headshot, LinkedIn URL, and email. It crops the headshot to a
gold-ringed circle, commits the 128px copy here as `<firstname>-headshot.png`,
builds the signature linking that URL, and hands over the paste-into-Gmail steps.
