# Profile README Redesign Plan

## Context
This repo is a GitHub profile README (`username/username` special repo) for the account `darynx`, display name **Deitzu** — a game-server hobbyist / beginner developer. The current `README.md` uses a tokyonight theme with a large GIF banner, a long bio, a featured-project block, and four stat widgets (two of which are broken). Goal: a **clean & minimal** redesign with a **dark base + teal accent**, removing images and fixing the dead/flaky stat widgets.

## Decisions (locked)
- **Theme:** Clean & minimal, dark background + teal accent.
- **Sections to keep:** minimal header, Interests & Learning, Tech Stack, Featured Project (compact), Stats widgets.
- **Intro/bio:** Restyle as a short centered header (`# Hi, I'm Deitzu` + one-line role), not the long paragraph.
- **Featured project:** Keep Darynxia but as a compact 2–3 line block.
- **Images:** Remove both `PixeLand ◇.gif` and `Messenger_creation_1498345494804187.jpg` (the Messenger image is unused; the GIF is the only referenced asset). README becomes typography-only.
- **Stats:** Replace dead/flaky widgets with working ones (see below).

## Custom teal palette (apply to all widgets for consistency)
- `bg_color=0d1117` (GitHub dark)
- `text_color=c9d1d9`
- `title_color=2dd4bf` (teal-400)
- `icon_color=5eead4`
- `border_color=30363d` (pass `&hide_border=true` where supported to drop the border instead)

## New README structure (top → bottom)
1. **Header** — centered `# Hi, I'm Deitzu` + one centered line: "Game-server hobbyist & beginner developer learning C#, Java, and JavaScript."
2. **Interests & Learning** — short bullet list (Game Servers, Development, Environments) kept but tightened.
3. **Tech Stack & Tools** — `skillicons.dev` with `&theme=dark` (or per-icon). Keep `cs,java,js,bash,gcp,linux,neovim`.
4. **Featured Project** — compact block:
   - **Darynxia** — cross-platform Terraria (TShock) server.
   - `darynxia.ddns.net:26018` · Terraria 1.4.5.6 · Cross-Play / FreeBuild
   - Listing: https://terraria-servers.com/server/5615/
5. **Stats** — two working widgets, both sharing the teal palette above:
   - Profile stats: `https://github-readme-stats.vercel.app/api?username=darynx&show_icons=true&theme=dark&hide_border=true&title_color=2dd4bf&icon_color=5eead4&text_color=c9d1d9&bg_color=0d1117&include_all_commits=true&show=reviews,issues,prs,contribs`
   - Top languages: `https://github-readme-stats.vercel.app/api/top-langs/?username=darynx&layout=compact&theme=dark&hide_border=true&title_color=2dd4bf&text_color=c9d1d9&bg_color=0d1117`
   - No streak, activity graph, snake, or summary-cards (kept minimal per user choice).

6. **Fun widgets** (added on top of the minimal stats):
   - **Visitor counter** — small profile-views badge, teal + flat-square to match:
     `https://komarev.com/ghpvc/?username=darynx&label=Profile%20Views&color=2dd4bf&style=flat-square`
     (reliable host; alternatively `visit-count` if ghpvc is down).
   - **GitHub trophies** — achievement badges, dark + clean (no frame/bg), themed tokyonight:
     `https://github-profile-trophy.vercel.app/?username=darynx&theme=tokyonight&no-bg=true&no-frame=true&margin-w=8`
     These add playful color without breaking the minimal layout.

## Implementation steps
1. Edit `README.md` to the new structure above (replace all 49 lines).
2. Delete `PixeLand ◇.gif` and `Messenger_creation_1498345494804187.jpg` (git rm).
3. Commit to `main` (the profile only renders from `main`/`master`). Current branch is a session branch — changes must land on `main`.

## Validation
- Open the rendered README on `https://github.com/darynx` (main branch) and confirm:
  - No broken image icons; profile stats + top-langs render with the teal palette.
  - Visitor counter badge renders with teal flat-square style.
  - Trophies render with tokyonight theme, no frame/bg (clean).
  - Skillicons render with the chosen icons.

## Risks / open items
- Both chosen widgets use `github-readme-stats.vercel.app`, which is generally reliable but depends on a third-party Vercel instance; if it goes down, both cards break simultaneously.
- Profile README only displays from the default branch — confirm repo default is `main` before committing there.
