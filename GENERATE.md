Auto-generation instructions
============================

1. Set environment variables:
```
export GIT_USER_ID=dojeda
export GIT_REPO_ID=quetzal-openapi-client
```
2. Run auto-generator script `./generate.sh`.
3. Review changes with `git status`.
4. Add update notes on `CHANGELOG.md`
5. Commit/push changes with `./git_push.sh $GIT_USER_ID $GIT_REPO_ID "<your commit message>"`
