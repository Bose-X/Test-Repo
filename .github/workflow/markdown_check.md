  
on: [pull_request, push]
name: Check markdown links
jobs:
  linkChecker:
    runs-on: ubuntu-latest
    steps:
      - name: markdownlint-cli
        uses: nosborn/github-action-markdown-cli@v1.1.1
        with:
          files: .
          ignore_files: "examples/ignore/*"
