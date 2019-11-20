Dockerfile can be found [here](https://github.com/ollikehy/backlog-app/blob/master/Dockerfile).
Changes can be viewed in the [commit-history](https://github.com/ollikehy/backlog-app/commit/57f4fe8d0f27010f7e27233ab04f17ca66bb89ed#diff-3254677a7917c6c01f55212f86c57fbf).

Size before and after: 1.01GB -> 142MB

Changes:
  - Changed python image to python:alpine
  - Instead of copying whole directory now copying only relevant files
  - Combining RUN-layers
  - Changed running user to a non-root user
