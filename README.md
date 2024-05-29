- `labeler-test` is a submodule to a repo (on a specific commit) containing an mdbook
- The CI in _this_ repo builds that book and publishes it from _this_ repo
- To update the book, the submodule just needs to be updated

Updating the submodule:
```bash
# new PR branch
git branch update
git switch update

# update submodule
cd $SUBMODULE_DIR
git checkout $DESIRED_COMMIT_OR_TAG
cd ../

# commit, send PR
git add $SUBMODULE_DIR
git commit -m '[...]'
git push
```

This was done in: https://github.com/hinto-janai/book-test/pull/1.
