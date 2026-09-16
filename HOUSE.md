# RooseveltAdvisors house fork

**Upstream:** https://github.com/mvanhorn/last30days-skill  
**House fork:** https://github.com/RooseveltAdvisors/last30days-skill (true GitHub fork)  
**Checkout:** `/opt/ra/firstmate/projects/last30days-skill` (firstmate project · direct-PR / yolo)

## Unique feature: Grok Build default X backend

When `grok` is installed and `~/.grok/auth.json` is signed in, unpinned runs use
**Grok Build** first for X discovery (`grok_x.py` → native `x_*_search` tools).

| | Upstream | House |
|---|---|---|
| Default X chain | bird → xai → xurl → xquik | **grok** → bird → xai → xurl → xquik |
| grok | opt-in pin only | default when auth present |
| Auth | cookies / XAI_API_KEY | Grok Build OAuth (quota-axi grok runway) |

Override anytime: `LAST30DAYS_X_BACKEND=bird|xai|xurl|xquik|xapi|grok`.

## Remotes / converge

```text
origin    RooseveltAdvisors/last30days-skill   (push house main)
upstream  mvanhorn/last30days-skill            (pull upstream)
```

```bash
git fetch upstream && git merge upstream/main   # or rebase
git push origin main
# then bump Zeta distribution.json commit / ref main
```
