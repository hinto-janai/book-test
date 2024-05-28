- `labeler-test` is a submodule to a repo (on a specific commit) containing an mdbook
- The CI in _this_ repo builds that book and publishes it from _this_ repo
- To update the book, the submodule just needs to be updated

Updating the submodule:
```bash
cd $SUBMODULE_DIR
git checkout $DESIRED_COMMIT_OR_TAG
cd ../

git add $SUBMODULE_DIR
git commit -m '[...]'
git push
```
