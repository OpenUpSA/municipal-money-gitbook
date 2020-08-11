# Development Operations

## Repository

{% embed url="https://github.com/OpenUpSA/municipal-data" %}

### Branches

**master** - Tracks the production version of the product.

**staging** - Tracks a version of the product that is based on production with additional un-reviewed branches merged in for review by product owner.

**feature-\[card\_number\]-\[description\]** - Tracks work on a feature that is based on the production version of the product.

**fix-\[card\_number\]-\[description\]** - Tracks work on a bug fix that is based on the production version of the product.

## Environments

### Production

Managed using a [Dokku](https://github.com/dokku/dokku) instance that is handled using a Git repository at the following URL: `dokku@dokku9.code4sa.org:municipal-finance`

### Staging

Managed using a [Dokku](https://github.com/dokku/dokku) instance that is handled using a Git repository at the following URL: `dokku@munimoney1-hetzner.openup.org.za:munimoney-staging-web`

