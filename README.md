# builder.xyz

Two sides of the same coin: professional + personal.

## Structure

```
builder.xyz/
├── content/              # Quartz markdown → personal digital garden
│   ├── garden.md        # Personal entry point (/garden/)
│   ├── reading.md       # Reading log
│   ├── interesting.md   # Links, talks, interesting things
│   ├── projects.md      # Tinkering, raspberry pi, etc.
│   └── notes.md         # Misc thoughts
│
├── static-pages/        # Hand-crafted HTML (landing + pro)
│   ├── index.html       # Landing: choose pro | personal
│   ├── landing.css      # Landing styling
│   └── pro/             # Professional section
│       ├── index.html   # Austin Fay, Division Order Analyst
│       └── style.css    # Pro styling (completely different)
│
├── build.sh              # Build script (Quartz + copy static)
├── quartz.config.yaml    # Quartz configuration
│
└── public/               # Output (created by build.sh)
```

## URLs

- `/` → Landing page (two paths)
- `/pro/` → Professional site (Austin Fay)
- `/garden/` → Personal entry point (The Workshop)
- `/reading/`, `/interesting/`, `/projects/`, `/notes/` → Personal content

## How to Use

### Writing Content (Personal Side)

Edit markdown files in `content/`:
- Add reading entries to `content/reading.md`
- Add interesting links to `content/interesting.md`
- Add project notes to `content/projects.md`
- Create new pages by adding new `.md` files

Link between pages using `[[page-name]]` syntax.

### With Obsidian

1. Open Obsidian
2. Open folder as vault: `builder.xyz/content/`
3. Edit, link, organize in Obsidian
4. Push to GitHub → site auto-builds

### Building Locally

```bash
npm ci                 # Install dependencies
npx quartz plugin install  # Install plugins
./build.sh             # Build (Quartz + static pages)
npx quartz build --serve  # Serve locally (before build.sh)
```

### Deploying

Push to `main` branch. GitHub Actions builds and deploys automatically.

## Design Philosophy

**Landing:** Minimal, brutalist, clear choice. Two panels, two paths.

**Professional:** Clean, restrained, competent. Typography-focused, minimal color. "I don't need to prove myself with flashy design."

**Personal:** Quartz digital garden. Graph view, backlinks, dark mode. Your raspberry pi, mezcal, two-stroke, earthen building side.