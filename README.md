# git-pre-commit-eslint
A git pre-commit hook for eslinting javascript files

Works by selecting all .js files modified (M) and added (A) in the git index. If any files match, file content is read using `git show :filename`. This ensures file data is read from git index and not disk as they can differ (lint-fixes could be made, but never added to index).
The content is now piped to eslint for the actual code check.
