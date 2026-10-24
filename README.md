# Marketing Skills

A library of skills for Claude Code. Each skill is a folder with a `SKILL.md` that tells
Claude how to do one job, a `README.md` that shows how to use it, and a `hero.webp`
thumbnail.

Open `index.html` in a browser to see the library page.

## Folder layout

```
index.html                       library page, one card per skill
README.md                        this file
skills/
  curiosity-gap-hooks/
    SKILL.md                     the instructions Claude loads
    README.md                    install, how to use, what to check
    EXAMPLES.md                  bad vs good, with the failed test named
    hero.webp                    thumbnail, 1200x675
```

## Install a skill

All projects:

```bash
mkdir -p ~/.claude/skills/curiosity-gap-hooks
cp skills/curiosity-gap-hooks/SKILL.md ~/.claude/skills/curiosity-gap-hooks/SKILL.md
```

One project only:

```bash
mkdir -p .claude/skills/curiosity-gap-hooks
cp skills/curiosity-gap-hooks/SKILL.md .claude/skills/curiosity-gap-hooks/SKILL.md
```

Start a new Claude Code session after installing.

## Add a skill

1. Create `skills/<skill-name>/`.
2. Write `SKILL.md` with a `name` and a `description` in the frontmatter. The description
   decides when Claude uses the skill, so list the phrases a user would actually type.
3. Write `README.md` with: what it does, install, how to use, how to read the output,
   when not to use it.
4. Write `EXAMPLES.md` with at least ten bad and good pairs. Each bad line names the
   check it fails. Each good line says why it works.
5. Add a `hero.webp` (1200x675) and a card in `index.html`.
