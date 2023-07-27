# Git merge issue

`git checkout --ours` and `git checkout --theirs` doesn't work correctly with the ort merge strategy.

1. `git checkout merge-test`
2. `git merge -s ort rename-my-file`
3. `git checkout --ours my-file3`

Notice how my-file3 still has merge conflict markers. You can run `git merge --abort` to cancel the merge.

1. `git checkout merge-test`
2. `git merge -s recursive rename-my-file`
3. `git checkout --ours my-file3`

Nitec how my-file3 now doesn't have conflict markers.
