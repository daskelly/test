# Test

This is a test repo.

Edited `.github/workflows/figshare_upload.yml` following
https://github.com/marketplace/actions/figshare-upload-action and
https://github.com/figshare/github-upload-action.

Get personal access token from Figshare -> Applications.
Then `gh set secret FIGSHARE_TOKEN`.

```bash
TAG=v0.5
git tag -a $TAG -m "new release test"
git push --follow-tags
gh release create $TAG
```

Disable the test workflow using
`gh workflow disable "github-actions-demo.yml"`

I set `.github/workflows/figshare_upload.yml` to upload
to figshare only on a new release being published, so it
won't release unless I execute the `gh release create` command
or create a release from the github webpage.

When a release is published, all the files get uploaded
to figshare. Moreover, the old files in that figshare item
are not deleted or overwritten. Instead, we now have copies of
both. We could delete the older copies if we wish.

