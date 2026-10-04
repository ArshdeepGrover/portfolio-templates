# Portfolio Starter

A single-file portfolio you can have online in about ten minutes.

No build step, no `npm install`, no framework, no dependencies. One
`index.html` you open in any editor, change the words, and deploy. It stays
that simple as it grows — adding a project is three more lines.

**[Use this template](../../generate)** → create your repository → edit →
deploy.

---

## What you get

- **Light and dark mode**, with a toggle. Follows the visitor's system
  setting; their choice is remembered.
- **Projects, skills and education** laid out the way people actually read a
  portfolio — work first.
- **An avatar** that draws your initials until you swap in a photo.
- **One colour variable** driving the whole page.
- **Responsive**, and it still renders correctly with JavaScript disabled.
- **No tracking, no analytics, no third-party requests.** Nothing loads from
  anyone else's server, so the page is fast and private by default.

---

## Quick start

### 1. Get the files

Click **Use this template → Create a new repository**, then edit `index.html`
directly on GitHub, or clone it and work locally:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO
open index.html          # Linux: xdg-open index.html
```

There is nothing to install. Opening the file in a browser is the dev server.

### 2. Replace three things

Everything editable is marked `[EDIT]` in the file. Start with Find & Replace
(`Ctrl+H`, or `Cmd+H` on a Mac):

| Find | Replace with |
|---|---|
| `YOUR NAME` | your name |
| `YOUR@EMAIL.COM` | your email |
| `yourusername` | your GitHub username |

Save, refresh the browser. That is already a working site.

### 3. Fill in the projects

The section that gets you replies. Three projects, three lines each, and a
number in every line.

> **Built a library system that tracks 500+ book records across 3 departments**

beats

> *Worked on a library management system project*

Not because the first is fancier — because it tells a reader what actually
happened. If those words already exist on your resume, copy them across rather
than rewriting them.

Need a fourth project? Copy a whole `<article class="project">` block. Only
have one? Delete the others. One real project beats three empty ones.

---

## Customising

### Colour

Two lines at the top of the `<style>` block:

```css
--accent:#C2410C;                   /* your colour */
--accent-soft:rgba(194,65,12,.10);  /* the same colour at 10% */
```

Change both and the whole page follows — buttons, links, chips, the avatar,
the accent edge on project cards.

| | Hex | Soft |
|---|---|---|
| Blue | `#2563EB` | `rgba(37,99,235,.10)` |
| Green | `#059669` | `rgba(5,150,105,.10)` |
| Purple | `#7C3AED` | `rgba(124,58,237,.10)` |
| Rose | `#E11D48` | `rgba(225,29,72,.10)` |

### Avatar

By default it draws your initials in a circle, coloured from `--accent`.
Change `YN` to your own two letters.

To use a photo: save it beside `index.html` as `photo.jpg`, delete the
`<svg class="avatar">` block, and uncomment the line just above it:

```html
<img class="avatar" src="photo.jpg" alt="YOUR NAME">
```

### Dark mode

Already working — nothing to configure. The page follows
`prefers-color-scheme`, and the button in the top-right corner overrides it.
The override is saved in `localStorage`, and a small inline script applies it
before first paint, so there is no flash of the wrong theme on load.

### Sections

There is a commented-out **Experience** block below Skills. When you have an
internship or a job, delete the two comment markers, fill it in, and move the
section above Skills. Education can shrink, or go entirely, once work history
earns the space.

Nothing on the page says "student". When that stops being true for you, you
change the words — not the website.

---

## Deploying

Any static host works, because it is one HTML file. Three easy ones:

**Vercel** — [vercel.com/new](https://vercel.com/new), import the repository,
set **Framework Preset: Other**, Deploy. (Or drag the folder onto
[vercel.com/drop](https://vercel.com/drop) and skip Git entirely.)

**Netlify** — [app.netlify.com](https://app.netlify.com), import the
repository, leave the build command empty and the publish directory as `/`.

**GitHub Pages** — Settings → Pages → Source: `main`, folder `/ (root)`. Live
at `yourusername.github.io/your-repo`.

Then put the link where people look: the top of your resume, your LinkedIn
headline, your email signature. Today, while you remember.

---

## Project structure

```
index.html    the whole site — HTML, CSS and about 30 lines of JS
README.md     this file
LICENSE       MIT
photo.jpg     optional, if you swap out the drawn avatar
resume.pdf    optional, linked from the header button
```

---

## Troubleshooting

| What you see | What to do |
|---|---|
| Page is blank | A stray `<` or `>`. Undo until it renders again |
| Colour didn't change | Only `--accent` and `--accent-soft` at the top. Change both |
| Dark mode looks wrong | You edited inside `:root[data-theme="dark"]`. Undo — you only ever change the accent |
| Avatar is a broken image | `photo.jpg` isn't beside `index.html`, or the filename differs |
| Vercel build fails | Framework Preset must be **Other**, not Next.js |
| Changes aren't live | Committed but not pushed, or the deploy is still running |

---

## Contributing

Issues and pull requests are welcome, particularly ones that keep the file
simple. The constraint is deliberate: **one file, no dependencies, no build
step.** A change that adds a package or a bundler is out of scope, however
nice the result.

## License

MIT — see [LICENSE](LICENSE). Use it, change it, ship it. Attribution is
appreciated but not required.
