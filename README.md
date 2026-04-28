# ezyshield docs

Mintlify documentation for the ezyshield API and product guides. Site configuration lives in [`docs.json`](docs.json); page content is MDX in this repo.

## Local preview

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) (or use `npx mint@latest dev`), then from the repo root:

```bash
mint dev
```

Open the URL the CLI prints (for example `http://localhost:3000`).

## Syncing the OpenAPI spec

The **API reference** tab is generated from [`api-reference/api.json`](api-reference/api.json). Regenerate that file from the main ezyshield application when API routes or schemas change (for example your project’s `composer docs` or equivalent export command). Commit the updated `api.json` here so deployed docs stay aligned with production.

After each export, spot-check the **Endpoints** sidebar for new tags (such as **ABA checks**) and skim operation descriptions.

## Contributing

- Follow the [Mintlify MDX reference](https://mintlify.com/docs) for components (`<Steps>`, `<Card>`, etc.).
- Prefer linking to generated operation pages under `/api-reference/…` (discover paths via `mint dev` and the sidebar).
- Avoid duplicating pagination, filtering, or full request/response schemas—link the API reference pages instead.

## Deployment

Connect the repo to Mintlify (GitHub app) so pushes to the default branch deploy the site. See [Mintlify deployment](https://mintlify.com/docs/deploy/deployments).
