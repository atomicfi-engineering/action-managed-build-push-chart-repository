<!-- start title -->

# GitHub Action:Managed Build and Push Chart to Registry

<!-- end title -->
<!-- start description -->

Builds and pushes a chart to a registry in a managed fashion for internal use

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: atomicfi/action-managed-build-push-chart-repository@undefined
  with:
    # Path to the chart to build and push. Required.
    # Default:
    chart-path: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**        | **Description**                     | **Default** | **Required** |
| :--------------- | :---------------------------------- | :---------: | :----------: |
| **`chart-path`** | Path to the chart to build and push |             |   **true**   |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start examples -->

### Example usage

```yaml
on: [push]

jobs:
  build-and-push-chart:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: atomicfi/action-managed-build-push-chart-repository@v1.0.0
```

<!-- end examples -->