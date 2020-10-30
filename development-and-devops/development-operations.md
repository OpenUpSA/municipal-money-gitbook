# Development Operations

## Repository

{% embed url="https://github.com/OpenUpSA/municipal-data" %}

### Branches

**master** - Tracks the production version of the product. Only merge into master if you are ready to deploy it to production right now. If you need to roll back a release, revert the merge commit and deploy the updated master branch.

~~**staging**~~ - Staging is just an environment. We do not batch features into staging and merge staging into master. We just deploy features to the staging environment to preview, and then merge the feature branch into master for release.

**feature-\[card\_number\]-\[description\]** - Tracks work on a feature that is based on the production version of the product.

**fix-\[card\_number\]-\[description\]** - Tracks work on a bug fix that is based on the production version of the product.

**preview-\[feature-\[feature\]\]** - When multiple feature branches are previewed in the staging environment, create a branch with that combination, and deploy to staging.

## Environments

### Production

Managed using a [Dokku](https://github.com/dokku/dokku) instance that is handled using a Git repository at the following URL: `dokku@dokku9.code4sa.org:municipal-finance`

### Staging

Managed using a [Dokku](https://github.com/dokku/dokku) instance that is handled using a Git repository at the following URL: `dokku@munimoney1-hetzner.openup.org.za:munimoney-staging-web`

