# Serversinc Deploy Trigger GitHub Action

Triggers a deployment in Serversinc by sending a CURL request to the API. Useful for automating deployments in CI/CD pipelines, such as after a successful docker build.

## Usage

```yaml
- name: Trigger Application Deployment
  uses: serversinc/deploy-action@v1
  with:
    hook: ${{ secrets.SERVERSINC_HOOK }}
    secret: ${{ secrets.SERVERSINC_SECRET }}
    tag: my-feature-branch
```

### Inputs
- `hook` (**required**): The deployment hook/event to trigger.
- `secret` (**required**): The deploy secret. Should be set from repository secrets.
- `tag` (optional): Docker Image tag to include in the deployment request body.

## License

MIT
