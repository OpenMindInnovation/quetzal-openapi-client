Auto-generation instructions
============================

1. Set environment variables:
```
export GIT_USER_ID=quetz-al
export GIT_REPO_ID=quetzal-openapi-client
```
2. Run auto-generator script `./generate.sh`.
3. Review changes with `git status`. One file that should be reverted is the `.gitignore`.
4. Commit/push changes with `./git_push.sh $GIT_USER_ID $GIT_REPO_ID "<your commit message>"`
5. (Optional) tag a release and push the tag. Use `v` as a prefix:
```
git tag -a vX.Y.Z -m "<Some meaningful tag message>"
git push --tags
```
