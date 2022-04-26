# Development Operations

## Repository

{% embed url="https://github.com/OpenUpSA/municipal-data" %}

### Branches

**master** - Tracks the production version of the product. Only merge into master if you are ready to deploy it to production right now. If you need to roll back a release, revert the merge commit and deploy the updated master branch.

~~**staging**~~ - Staging is just an environment. We do not batch features into staging and merge staging into master. We just deploy features to the staging environment to preview, and then merge the feature branch into master for release.

**feature-\[card\_number]-\[description]** - Tracks work on a feature that is based on the production version of the product.

**fix-\[card\_number]-\[description]** - Tracks work on a bug fix that is based on the production version of the product.

**preview-\[feature-\[feature]]** - When multiple feature branches are previewed in the staging environment, create a branch with that combination, and deploy to staging.

## Environments

### Production

Managed using a [Dokku](https://github.com/dokku/dokku) instance that is handled using a Git repository at the following URL: `dokku@dokku9.code4sa.org:municipal-finance`

### Staging

Managed using a [Dokku](https://github.com/dokku/dokku) instance that is handled using a Git repository at the following URL: `dokku@munimoney1-hetzner.openup.org.za:munimoney-staging-web`

## Environment variables

GOOGLE\_ANALYTICS\_DATA - Google Analytics ID for the data explorer site

GOOGLE\_ANALYTICS\_SCORECARD - Google Analytics ID for the Municipal Money main site&#x20;

NO\_INDEX - Setting this to anything will disable search engine indexing for that environment

## Useful commands

### Database dump

```bash
docker run --rm -v $PWD:/data postgres:11.5 pg_dump -O -c --if-exists $(dokku config:get municipal-finance DATABASE_URL) | gzip > municipal-finance-prod-$(date "+%Y-%m-%d-%H00").sql.gz
```

### Database dump without Django and auth data

```bash
docker run --rm -v $PWD:/data postgres:11.5 pg_dump -O -c --if-exists $(dokku config:get municipal-finance DATABASE_URL) -T 'auth_*' -T 'django_*' | gzip > municipal-finance-prod-clean-$(date "+%Y-%m-%d-%H00").sql.gz
```

### Database dump only Django and auth data

```bash
docker run --rm -v $PWD:/data postgres:11.5 pg_dump -O -c --if-exists $(dokku config:get municipal-finance DATABASE_URL) -t 'auth_*' -t 'django_*' | gzip > municipal-finance-prod-auth-$(date "+%Y-%m-%d-%H00").sql.gz
```

### Database import

```bash
zcat < municipal-finance-prod-XXXX-XX-XX-XXXX.sql.gz | docker-compose run --rm postgres psql postgresql://municipal_finance@postgres/municipal_finance
```
