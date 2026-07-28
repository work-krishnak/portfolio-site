# Build Log — Portfolio Project

## Phase 1 — Portfolio

### Step 10 — Connect to GitHub remote
What broke: Ran `git remote add origin ...` twice — first time with the literal
placeholder "YOUR-USERNAME" still in the URL (copied from Claude's example instead
of GitHub's actual page text), which created a broken remote. Second attempt with
the real username failed with `error: remote origin already exists.`

What Claude got wrong: The instruction said "copy the first two lines exactly as
GitHub shows them" but didn't warn clearly enough about not running the example
text shown in the prompt itself before checking GitHub's actual page.

How we recovered: Ran `git remote set-url origin https://github.com/work-krishnak/portfolio-site.git`
to overwrite the bad remote instead of adding a new one. Verified with `git remote -v`.

Time spent: ~5 minutes from error to confirmed fix.

## Phase 1 — Summary

Live URL: https://work-krishnak.github.io/portfolio-site/
GitHub repo: https://github.com/work-krishnak/portfolio-site
Status: Complete and verified live.
Main issue encountered: git remote setup (see Step 10 log above).
No other blockers.

## Known issue to revisit
Global git email/name were unset during Phase 1, so portfolio-site commits used
an auto-guessed identity (v-kumarchak@microsoft.com) instead of the intended
work.krishnak@gmail.com. Needs amending before final submission.