Dockerfile can be found [here](https://github.com/ollikehy/backlog-app/blob/master/Dockerfile).
Changes can be viewed in the [commit-history](https://github.com/ollikehy/backlog-app/commit/88f62b4f1ae3c3250d4b88ee6ce01778db29a235).

Size before and after: 1.01GB -> 142MB

Changes:
  - Changed python image to python:alpine
  - Instead of copying whole directory now copying only relevant files
  - Combining RUN-layers
  - Changed running user to a non-root user