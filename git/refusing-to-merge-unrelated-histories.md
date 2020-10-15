# Refusing to Merge Unrelated Histories

For example, I created a new repository locally, then created a new repository
on GitHub. However GitHub had changed their default branch to `main`. When
I added GitHub as a remote to my local repository I renamed my local default
branch to match the remote. So far, so good. When I tried to merge my local
changes with the remote though I got the error:

```
fatal: refusing to merge unrelated histories
```

The fix was pretty straightforward, as this was a new repo with minimal
commits:

```
git branch -m main
git fetch origin
git merge origin/main --allow-unrelated-histories
```

YMMV though. `--allow-unrelated-histories` should only be used if you're sure
you need to use it.

[Detailed explanation](https://stackoverflow.com/a/39783462).
