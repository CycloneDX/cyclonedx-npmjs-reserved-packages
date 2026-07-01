# CycloneDX npmjs reserved packages

This repository contains placeholder npm packages published under CycloneDX-related names to prevent name-squatting and
typosquatting in the npm registry.

All packages here are intentionally empty.  
Official CycloneDX JavaScript packages are published under the scope `@cyclonedx`:

<https://www.npmjs.com/search?q=%40cyclonedx>

## Structure

```text
packages/
  cyclonedx/
  cyclonedxjs/
  ...
```

Each package includes a minimal `package.json` and a README pointing users to the official namespace.

## Publishing the reserved packages

This repository includes a GitHub Actions workflow that publishes all packages in the `packages/` directory to npm.  
The workflow is named **“Publish all npm packages”** and can be triggered manually.

### How to run it

1. Go to **GitHub → Actions** in this repository.
2. Select **Publish all npm packages** from the workflow list.
3. Click **Run workflow**.
4. Confirm the dialog and start the run.

The workflow will:

- discover all package directories under `packages/`
- run a matrix job to publish each package individually
- skip packages that are already published

## License

Apache-2.0
