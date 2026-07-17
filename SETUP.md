# How to set this up

GitHub profile READMEs only work from a special repo named **exactly your username**.

## 1. Create the special repo
- Go to GitHub → New repository
- Name it `Shitanshu06` (must match your username exactly)
- Make it **public**
- Check "Add a README file"

## 2. Add the files
- Replace the auto-generated `README.md` with the one in this folder.
- Add the `assets/ascii-portrait.svg` file too (it's your photo converted to a
  self-typing ASCII terminal portrait) — the README links to it at
  `./assets/ascii-portrait.svg`.
- Create the folder `.github/workflows/` in that repo and add `snake.yml` there.

## 3. Enable Action permissions
- In the repo: Settings → Actions → General → Workflow permissions
- Select **"Read and write permissions"** and save.
- This lets the snake action commit the generated SVG to an `output` branch.

## 4. Run it once manually
- Go to the **Actions** tab → "Generate Snake Animation" → **Run workflow**
- After it finishes, an `output` branch will appear with the SVG files.
- The README already points to that branch, so the snake image will show up automatically.

## 5. (Optional) swap the theme
- The stats cards and typing text use `theme=synthwave` and a green terminal color.
  Change `theme=synthwave` to `radical`, `dracula`, `tokyonight`, etc. on the
  github-readme-stats / streak-stats URLs if you want a different palette.
- The typing text color is controlled by `&color=39FF14` in the typing-svg URL —
  swap the hex code for any color you like.

That's it — everything else (typing animation, stats cards, streak, language
breakdown) is rendered live by free public services, so it always stays current
with zero maintenance. Only the snake needs the daily Action to redraw itself.
