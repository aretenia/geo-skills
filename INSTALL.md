# Install

These are Claude Code skills. Installing them means placing the skill folders where Claude Code looks for them.

## Quick install (manual)

```bash
git clone https://github.com/SmokeAlot420/geo-skills.git
cd geo-skills

# copy the skills into your Claude Code skills directory
cp -r skills/* ~/.claude/skills/

# copy the orchestrator's subagents
cp -r agents/* ~/.claude/agents/
```

On Windows (PowerShell):

```powershell
Copy-Item -Recurse skills\* $HOME\.claude\skills\
Copy-Item -Recurse agents\* $HOME\.claude\agents\
```

Restart Claude Code (or reload skills) so it picks up the new skills.

## Use it

```
/geo audit https://yoursite.com
```

That runs the full audit and returns your GEO Score plus a prioritized fix list. Other entry points:

```
/geo page https://yoursite.com/specific-page
/geo llmstxt https://yoursite.com
/geo-audit https://yoursite.com
```

You can also call individual skills directly, e.g. `geo-citability`, `geo-crawlers`, `geo-schema`.

## Optional dependencies

The core audit needs nothing beyond Claude Code. A couple of skills use optional Python packages only if you invoke them:

- `geo-report-pdf` (PDF reports) - needs `reportlab`
- `geo-prospect` / the CRM dashboard in `geo` - needs `flask`

Install them only if you use those features:

```bash
pip install reportlab flask
```

No SEO API keys are required for any skill. Third-party data tools (rank trackers, backlink suites) are always optional and the skills degrade gracefully without them.
