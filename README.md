# git-utils
Some scripts and utilities to make working with git a bit more convenient
Place them somewhere in your `$PATH` and run `chmod +x` on them, to use them.

## git commit-branch

Usage: `git commit-branch <target-branch> [--rebase|-r] [ <git-commit-options>... ]`

Commits your staged changes to `<target-branch>`, discarding them from your current branch.
Use `--rebase` or `-r` to rebase your current branch on the new commit in `<target-branch>`,
and thus include the changes in your current branch as well.

Example usage working on branch my-feature:

```bash
# Working on branch 'my-feature', finding a bug in 'some-file'...
git add -p some-file
git commit-branch main --rebase -m 'Fixed a bug in some-file'
```
