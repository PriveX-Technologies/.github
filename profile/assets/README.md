# Asset Manifest

Reference for every image in `profile/assets/` — what it depicts, its canonical alt
text, and where it appears in the [org profile README](../README.md). If you change an
image or its alt text here, update the README to match (and vice versa).

| File | One-line summary | Canonical alt text | Used in |
|------|------------------|--------------------|---------|
| `hero.svg` | Animated dark banner reading **"PRIVEX TECHNOLOGIES — ENGINEERING INTELLIGENT SYSTEMS"** with domain chips (software, AI, hardware, IoT, security, R&D), circuit mesh and glowing particles | `Privex Technologies — Engineering Intelligent Systems. Software · AI · Hardware · IoT · Security · R&D` | Page header |
| `icon-ai.svg` | Rounded-square icon: robot face with radiating signal lines | `AI & Intelligent Systems` | Core Domains · AI cell |
| `icon-iot.svg` | Rounded-square icon: device under radio waves | `IoT & Embedded Systems` | Core Domains · IoT cell |
| `icon-security.svg` | Rounded-square icon: shield with a check mark | `Security Engineering` | Core Domains · Security cell |
| `icon-rt.svg` | Rounded-square icon: monitor drawing a live waveform trace | `Real-Time & Interactive Technology` | Core Domains · Real-time cell |
| `icon-software.svg` | Rounded-square icon: code brackets `< / >` | `Software & Platforms` | Core Domains · Software cell |
| `icon-rnd.svg` | Rounded-square icon: magnifying glass over a pulsing target | `Research & Development` | Core Domains · R&D cell |
| `divider-a.svg` | Animated gradient divider bar (purple → blue → red), fading at both ends | *(empty — decorative)* | Section separators: header, Projects, footer |
| `divider-b.svg` | Animated gradient divider bar (blue → purple → red), fading at both ends | *(empty — decorative)* | Section separators: Projects, footer |
| `divider-c.svg` | Animated gradient divider line with pulsing end nodes and dashed mid-segments | *(empty — decorative)* | Section separators: Who We Are, Engineering Principles, Vision |

## Notes

- **Alt text is what counts.** Each SVG carries internal `<title>` / `<desc>` /
  `aria-label` metadata for standalone viewing, but when embedded with `<img>` (the way
  the README uses them) only the `alt` attribute is announced — the "Canonical alt text"
  column above is the source of truth for the README.
- **Dividers intentionally use empty alt** (`alt=""` in the README): they are purely
  decorative, so screen readers skip them instead of reading "divider" six times.
- **Icon alt matches the badge beside it** so the icon stays meaningful if shields.io
  is unreachable or rendering falls back to alt text; screen-reader users may hear the
  domain name twice, which is an accepted trade-off.
- **All images animate via SMIL** (no scripts). The motion is decorative and carries no
  information, so nothing is lost in static contexts. If reduced motion ever becomes a
  requirement, add static variants and swap them via the README.
