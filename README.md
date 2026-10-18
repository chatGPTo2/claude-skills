# chathuka-skills

Personal Claude skills, packaged as a plugin marketplace. Works in Claude Code
and in claude.ai chats.

## Plugins

| Plugin | What it does |
| --- | --- |
| kids-book | Children's picture book production: story style, character bibles, page breakdowns, image prompts, KDP specs |

## Install in Claude Code

```
/plugin marketplace add YOUR_GITHUB_USERNAME/claude-skills
/plugin install kids-book@chathuka-skills
```

Add `--scope project` to the install to share it with a specific repo.

## Install in claude.ai

Settings, then the plugins section, then the **Added** tab, then **Add Marketplace**.
Choose **Add from a Repository** and paste this repo's URL. Install the plugin
from the list. The skill then triggers on its own in any chat.

## Updating

Push changes to this repo, then in Claude Code:

```
/plugin marketplace update chathuka-skills
```

## Adding another skill

1. Create `plugins/<name>/.claude-plugin/plugin.json`
2. Create `plugins/<name>/skills/<name>/SKILL.md`
3. Add an entry to the `plugins` array in `.claude-plugin/marketplace.json`

The `description` line in SKILL.md frontmatter is what Claude matches against to
decide whether to load the skill, so make it concrete about when it applies.
