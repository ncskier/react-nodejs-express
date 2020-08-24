# React Node.js Express Stack Kabanero Integration

Add this React Node.js Express stack to your kabanero instance by adding the
following lines to your cluster's `kabanero` CRD's `stacks` section:

```yaml
stacks:
  repositories:
    - https:
        url: https://github.com/ncskier/react-nodejs-express/raw/master/ci/assets/dev.local-index.yaml
      name: bcwalker
      pipelines:
        - https:
            url: https://github.com/ncskier/react-nodejs-express/raw/master/ci/assets/default-kabanero-pipelines.tar.gz
          id: bcwalker
          sha256: c8bd01c33a4e28867a2bb583f12a52d0f5d13a78a1ee111a0fd54ff965fa1072
```

For the v0.1.0 release, use:

```yaml
stacks:
  repositories:
    - https:
        url: https://github.com/ncskier/react-nodejs-express/releases/download/v0.1.0/dev.local-index.yaml
      name: bcwalker
      pipelines:
        - https:
            url: https://github.com/ncskier/react-nodejs-express/releases/download/v0.1.0/default-kabanero-pipelines.tar.gz
          id: bcwalker
          sha256: c8bd01c33a4e28867a2bb583f12a52d0f5d13a78a1ee111a0fd54ff965fa1072
```
