# Poolser website

Read README.md for this repository's scope. Before interface changes, read the shared guide at https://github.com/poolser-app/brand/blob/main/BRAND.md and the consumer's pinned version once adopted. Keep local implementation guidance up to date with visual and interaction changes. Preserve financial data semantics, truthful unavailable states, light/dark appearance, keyboard/screen-reader access and reduced motion.

Use the original Poolser artwork from a reviewed brand commit. Keep required assets local and record the adopted commit; do not fetch mutable brand files at runtime or during builds. Never commit credentials, real wallet configuration or private portfolio captures.

Shared policy source: [native AGENTS.md at 2156823](https://github.com/poolser-app/native/blob/215682391bcacc9ccb55f2e051bddd608512b42f/AGENTS.md). The shared section below is copied locally; no external include is required. Synchronize it with the canonical native section when that policy changes.

<!-- shared-poolser-rules:start -->
## Shared Poolser rules

### Authorship and public text

- Do not add AI co-authors or attribution trailers (`Co-Authored-By`, `Generated-by`, `Assisted-by`, `Signed-off-by` or equivalents naming an assistant, model, bot or vendor).
- Do not mention or imply AI/tool authorship in commits, branch names, PR titles/bodies, issues, review comments, release notes, tags, changelogs, store copy, product UI, source comments, logs or public documentation. No generated-with footers, badges or robot signatures. Describe the change and its reason in the repository owner's voice.
- Tool configuration files (`AGENTS.md`, `CLAUDE.md`, `.agents/`, `.claude/` and `.githooks/`) may state these instructions and tool configuration; this exception does not allow authorship narratives or attribution.
- Use only the configured Git identity. Never override `--author`, change `user.name`/`user.email`, or set `GIT_AUTHOR_*`/`GIT_COMMITTER_*`.
- Use Conventional Commits with an imperative, lower-case summary (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`, `revert:`). Use purpose-based branch names such as `feat/native-network-support` or `chore/repository-guidance`, without tool/model/vendor prefixes.
- Before every commit, push or PR, review the message, public text and staged diff for these rules; tooling-policy files above are exempt from the text scan. Enable repository hooks with `git config core.hooksPath .githooks`. Install `gitleaks` before committing; do not bypass hooks. The commit-message hook checks attribution; the pre-commit hook checks staged secrets.

### Scope, security and verification

- Read the local README, relevant instructions and existing implementation before editing. Make the smallest complete change that solves the task, using existing helpers and dependencies. Preserve unrelated work and keep each task reviewable.
- Never commit credentials, project API keys, signing material, private wallet configuration or real/private portfolio captures. Use fictional fixtures or sanitized public-chain evidence. Do not log credential-bearing URLs or raw provider errors.
- Keep scratch plans, transcripts, temporary scripts and conversational summaries outside the repository. Commit only maintained product/engineering documentation. Source comments explain why; no chat-style or generated-code annotations, empty scaffolding or unfinished TODO stubs.
- Preserve exact financial integer math, token decimals, quote/range orientation and the difference between known zero, unavailable, partial, syncing and stale. Realized APR must remain distinct from estimated pool yield. Do not fabricate history, returns, availability or progress.
- Run checks appropriate to the change. New nontrivial financial/security/storage logic needs meaningful fixtures or tests; documentation-only changes need link/diff checks, not unrelated full application builds. Report what actually passed and any material verification gap.
- Do not silently merge unrelated/open predecessor PRs, deploy, publish or alter accounts as an implementation shortcut. Follow the task's authorized scope and explicit dependencies.

### Shared design and repository boundaries

- Before interface changes, read the local `docs/BRAND.md` and pinned shared guide when present; `poolser-app/brand` is the shared identity source. Update the owning guide alongside changes to palette, typography, motion, hierarchy or platform interaction.
- Preserve original artwork, semantic colours, numeric formatting, accessibility, light/dark appearance and reduced motion. Keep adopted brand assets/tokens local at a reviewed commit; builds and runtime must not fetch mutable brand files or require another repository checkout.
- Reuse established Poolser product labels and approved copy. Avoid invented slogans and repeated headings/field labels. The web application follows native financial meaning and hierarchy, adapting platform interactions rather than inventing a separate product design.
- Keep application-specific implementation in its owner: native for Mac/iOS/widgets, web for browser monitoring/collection, website for presentation/downloads/support/privacy, brand for shared identity/assets/tokens, `.github` for organization presentation and coordination.
<!-- shared-poolser-rules:end -->

## Website repository checks

This repository owns the landing page, downloads, Go to app, support and public privacy information. The working portfolio/collection application belongs to poolser-app/web. Use actual native captures with fictional data and only confirmed platform/download/domain/contact claims. Do not imply an unavailable store release is published. Keep the Uniswap non-affiliation statement.

Adopt local brand assets before UI work and record their revision. Run this repository's actual build/check scripts once implemented; verify the real HTTP preview, links, responsive layout, keyboard access, contrast and reduced motion. Do not introduce accounts, tracking, RPC credentials or application features as landing-page scaffolding.
