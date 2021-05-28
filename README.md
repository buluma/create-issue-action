# Create Issue Action
[![Test Workflow](https://github.com/buluma/create-issue-action/actions/workflows/test.yaml/badge.svg)](https://github.com/buluma/create-issue-action/actions/workflows/test.yaml)

This will let you create an issue based on user input from your GitHub Workflow

## Inputs
### title
**Required** - Title of the issue
### token
**Required** - Token of user that will create issue
### assignees
**Not Required** - Assignes of the issue
### labels
**Not Required** - Labels of the issue
### body
**Not Required** - Body of the issue

## Usages
```yaml
- uses: buluma/create-issue-action@v2.0.0
  name: Create Issue Action
  with:
    title: Build Failed
    token: ${{secrets.GITHUB_TOKEN}}
    assignees: ${{github.actor}}
    labels: worflow-failed
    body: Workflow failed for commit ${{github.sha}}
```
