# Claude Code revision and dirty-checkout procedure

Observed 2026-10-11. Supported host: Claude Code with native subagents and Git worktrees. Record the installed `claude --version` and inspect local help/configuration before applying current documentation to an older host. This package adds no agents or runtime.

## Documented behavior

[Claude Code subagents](https://code.claude.com/docs/en/sub-agents), Frontmatter reference: `isolation: worktree` defaults to the default branch, not the parent's HEAD. Naming a feature branch in a brief does not configure this field. No-change worktrees are automatically removed.

## Package procedure

1. Freeze the required input snapshot before workers edit: record the parent repository root, `git rev-parse HEAD`, `git status --porcelain=v1`, and approved input paths. Keep the existing session cap. Do not commit, stash, reset, or clean the user's checkout to transport it.
2. Export authorized tracked changes relative to that HEAD with `git diff --binary HEAD -- <approved paths>` into an owned file outside the checkout. This combines staged and unstaged changes; patches do not carry untracked files. Inventory and copy required untracked files separately, preserving paths, bytes and executable modes; exclude unrelated files and secrets. Record hashes of the required input files, deletions and modes. Handle submodule contents separately; a superproject patch is insufficient for dirty submodules.
3. Launch through native isolation with a preparation-and-coding brief. Keep that invocation active through preparation; completing a no-change preparation run can trigger automatic worktree removal. Before coding, each worker reports `pwd`, `git rev-parse --show-toplevel`, `git rev-parse HEAD`, and status. Confirm distinct worker roots, neither equal to the parent. If HEAD differs, in the new, clean, owned worktree use `git switch --detach <recorded parent SHA>` before applying changes. If the host cannot safely keep the worker at this revision, serialize in an authorized location. Never force a switch over unexpected edits.
4. Run `git apply --check <patch>` in each worker root, then `git apply <patch>`. Copy the approved untracked inputs. Compare hashes, modes and expected absences against the snapshot, including API contract files needed by both workers. Only then release coding assignments. Concurrent changes to the parent's inputs invalidate this snapshot and require a new one.
5. Keep the prepared dirty snapshot as the worker baseline. Integrate only each worker's subsequent delta, excluding the transported parent edits; reapplying the entire diff would duplicate the user's changes. Verify combined behavior and preserve conflicting outputs.

This is a package procedure built from documented Git operations, not a claim that native isolation imports dirty files automatically. Git sources, opened 2026-10-11: [git diff](https://git-scm.com/docs/git-diff) (`HEAD`, path filtering, binary patches); [git apply](https://git-scm.com/docs/git-apply) (`--check` checks applicability without applying); [git worktree](https://git-scm.com/docs/git-worktree) (separate working trees sharing repository objects); [git switch](https://git-scm.com/docs/git-switch) (`--detach` at an explicit commit).

All URLs were opened successfully on the observation date. Recheck installed behavior if host/version differs; do not transfer Claude-specific defaults to other hosts.
