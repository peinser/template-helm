# Helm Repository

A template repository for managing Helm charts specific to a single project.

--------------------------------------------------------------------------------

> [!WARNING]
> Work in progress.

## Configuration

### GitHub

### GitLab

A group or project access token needs to be created with the name `cicd`. The token should have the `write_repository` permissions.

#### HTTP

```bash
helm repo add reponame https://raw.githubusercontent.com/peinser/template-helm/main/repo
```

The above only works for public repositories. Otherwise, registry credentials such as SSH keys or a PAT are required.

#### OCI Artifact

Alternatively, it is possible to configure an OCI compatible container registry to manage Helm charts. To enable
this behaviour, the following variables (and secret) have to be defined:

- `HELM_OCI_REGISTRY`
- `HELM_OCI_USERNAME`
- `HELM_OCI_SECRET`

## Changelogs

## Conventions

- We use the Helm `.Release.Name` as an identifier for the environment. That is, your deployment's name will be `{{ .Release.Name }}-sample`.

## Repository secrets
