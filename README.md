# Hello World Action

A minimal dummy GitHub Action that prints "Hello, World!".

## Usage

In a workflow (`.github/workflows/*.yml`):

```yaml
jobs:
  hello:
    runs-on: ubuntu-latest
    steps:
      - uses: ./
```

Or from another repo after publishing:

```yaml
- uses: your-org/actions-poc@main
```

## Local test

From this repo root:

```bash
docker run --rm -v "$(pwd):/action" ghcr.io/actions/runner:latest /action/action.yml
```

Or trigger via a workflow that uses `uses: ./` in this repository.
