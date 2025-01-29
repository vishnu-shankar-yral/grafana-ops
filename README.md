# grafana-ops

IaC ops repo for Grafana

## Runbook for setting up grafana

-   Create volume on fly
-   Create oauth credentials for google sign in
-   Create fly secrets
-   Edit fly.toml file to appropriate config
-   Lunch fly grafana app using `fly.toml`
-   Create a role and service account for grafana
-   Add grafana bigquery data source

## Grizzly dashboard editing workflow

-   Obtain service account for google big query access
-   Create google big query data source

## Secret environment variables

-   GF_AUTH_GOOGLE_CLIENT_ID
-   GF_AUTH_GOOGLE_CLIENT_SECRET

## References for runbook

-   [Environment variables](https://grafana.com/docs/grafana/latest/setup-grafana/configure-grafana/)

-   [Deploy as docker container](https://grafana.com/docs/grafana/latest/setup-grafana/installation/docker/)

-   [Google oauth setup](https://grafana.com/docs/grafana/latest/setup-grafana/configure-security/configure-authentication/google/#configure-google-oauth2-authentication)

-   [Create service account for big query](https://cloud.google.com/iam/docs/service-accounts-create)

    -   Custom role permissions
        ```
        bigquery.datasets.get
        bigquery.jobs.create
        bigquery.models.export
        bigquery.models.getData
        bigquery.models.getMetadata
        bigquery.models.list
        bigquery.routines.get
        bigquery.routines.list
        bigquery.tables.export
        bigquery.tables.get
        bigquery.tables.getData
        bigquery.tables.list
        resourcemanager.projects.get
        ```
