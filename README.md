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
- uses: atomicfi-engineering/action-managed-build-push-chart-repository@undefined
  with:
    # Path to the chart to build and push. Required.
    # Default:
    chart-path: ""
    # AWS access key id. Required.
    # Default:
    aws-access-key-id:
    # AWS secret access key. Required.
    # Default:
    aws-secret-access-key:
```

<!-- end usage -->
<!-- start inputs -->

| **Input**                   | **Description**                     | **Default** | **Required** |
| :-------------------------- | :---------------------------------- | :---------: | :----------: |
| **`chart-path`**            | Path to the chart to build and push |             |   **true**   |
| **`aws-access-key-id`**     | AWS access key id                   |             |   **true**   |
| **`aws-secret-access-key`** | AWS secret access key               |             |   **true**   |

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
      - uses: atomicfi-engineering/action-managed-build-push-chart-repository@v1.0.0
        with:
          chart-path: ./charts/my-chart
          aws-access-key-id: ${{ secrets.YOUR_AWS_ACCESS_KEY_ID }}
          aws-secret-access-key:  ${{ secrets.YOUR_AWS_SECRET_ACCESS_KEY }}
```

<!-- end examples -->