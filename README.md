download-release-assets
=======================

This action downloads a specific release's asset by matching asset name.

Usage
-----

Download asset from the latest release:

```yaml
- uses: houqp/download-release-assets@v1
  with:
    repo: houqp/terraform-provider-airflow
    match: "terraform-provider-airflow_.+_Linux_386.tar.gz$"
    rename: terraform-provider-airflow
```

Download asset for a specific release:

```yaml
- uses: houqp/download-release-assets@v1
  with:
    release: v1.0.0
    repo: houqp/terraform-provider-airflow
    match: "terraform-provider-airflow_.+_Linux_386.tar.gz$"
    rename: terraform-provider-airflow
```

Download asset from a private repo using personal access token:

```yaml
- uses: houqp/download-release-assets@v1
  with:
    token: {{ secrets.GITHUB_PAT }}
    repo: houqp/terraform-provider-airflow
    match: "terraform-provider-airflow_.+_Linux_386.tar.gz$"
    rename: terraform-provider-airflow
```
