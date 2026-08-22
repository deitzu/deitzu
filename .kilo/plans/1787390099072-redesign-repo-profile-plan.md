# Repo Profile README Redesign Plan

## Goal
Redesign the GitHub profile README (`README.md`) with both visual style refresh and content reorganization, keeping the "Deitzu" personal brand identity.

## Constraints
- Must remain a valid GitHub-flavored Markdown README
- Keep core identity: "Hi, I'm Deitzu" header and personal branding
- Profile lives at root `README.md` level
- Use publicly available APIs/services only (GitHub badges, skillicons, etc.)

## Affected Boundaries
- Single file: `README.md` at repo root
- No backend changes, no new services
- All data sourced from existing/github APIs or manually updated

## Data Flow
- Static Markdown content with embedded badges/links
- GitHub stats badges fetch from `github-readme-stats.vercel.app`
- Skill icons from `skillicons.dev`
- Custom badges and assets hosted or from external services

## Visual Style Direction
- **Theme**: Tokyo Night (already used, keep for consistency) with modern accent colors
- **Typography**: System font stack, larger header hierarchy
- **Layout**: Grid-based two-column for stats, centered content sections
- **Spacing**: Consistent 4px/8px vertical rhythm, generous white space
- **Accent colors**: Secondary accent (e.g., cyan/teal) for highlights, keeping primary as current scheme

## Content Reorganization
### Current sections kept:
1. Header: "Hi, I'm Deitzu" - keep as primary branding
2. About paragraph - condense/update
3. Animated GIF - keep but optimize positioning
4. Interests & Learning - restructure as categories/tags
5. Tech Stack & Tools - update icon set, keep skillicons format
6. Featured Project - update Darynxia info or replace with current focus
7. Stats badges - keep layout, update usernames/filters

### New/Enhanced sections:
- **Contact & Social**: GitHub, email, Twitter/Mastodon links
- **Recent Activity**: Dynamic or recent commits/repos (optional)
- **Skills Badge**: Compact summary of top skills
- **Achievements/Badges**: Display any earned badges/certifications

## Tech Stack & Icons
- Current: `cs,java,js,bash,gcp,linux,neovim`
- Recommendation: Add/remove based on current learning/focus
- Use skillicons dev format with consistent spacing
- Add dark/light mode variants where possible

## Project Showcase
- Update Darynxia Terraria server info
- Or: Replace with current primary project with status badges
- Include: address, version, features, links
- Add "Last updated" timestamp

## GitHub Stats
- Keep existing badge layout (4 stats + 4 lang badges + 2 streak cards)
- Update username from `darynx` to match current GitHub handle
- Filter: `reviews,issues,prs,contribs` kept; add `commits` if desired
- Themes: Tokyo Night consistent

## Failure Modes & Validation
- Badges 404-ing: Use fallback images or remove broken badges
- Skillicons icon missing: Use generic placeholder
- GitHub stats unavailable: Graceful degradation to text
- Rendering on GitHub: Verify final README renders correctly

## Rollout Plan
1. Write new `README.md` content
2. Test rendering locally (if possible) or via GitHub preview
3. Commit and push to `main`
4. Monitor first 24h for rendering issues
5. Iterate based on feedback

## Open Questions (for user clarification)
1. Primary color accent preference (keep cyan, switch to magenta, or custom)
2. Whether to keep Darynxia server or replace with current project
3. Any social links to add (Twitter, Mastodon, personal site)
4. Desired stat filters beyond current `reviews,issues,prs,contribs`

---
*Plan generated for repo profile redesign. Ready for implementation once user confirms open questions.*