# Test

This is a test repo.

Edited `.github/workflows/figshare_upload.yml` following
https://github.com/marketplace/actions/figshare-upload-action and
https://github.com/figshare/github-upload-action.

Get personal access token from Figshare -> Applications.
Then `gh set secret FIGSHARE_TOKEN`.

```bash
git tag -a v0.4 -m "new release test"
git push --follow-tags
gh release create v0.4
```

Disable the test workflow using
`gh workflow disable "github-actions-demo.yml"`

