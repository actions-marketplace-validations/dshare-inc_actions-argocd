# 🚀 Actions - ArgoCD
> ArgoCD 환경에 배포하기 위한 D-SHARE Inc. 전용 YAML 에디터입니다.

```yaml
name: 🔍 Test

on: push

jobs:
  Test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: dshare-inc/actions-argocd@1.0.0
        with:
          action: put
          manifest_path: values.yaml
          enable_update: false
          enable_permanent_protection: true
          env: dev
          key: '183'
          lifecycle: temporary
          image_tag: DOCKER_IMAGE_TAG_V1
          deployment_strategy: blue_green
          action_type: push
          action_worker_number: 7123c79a-f2c9-4cb4-af10-f06bf18d68b6
          action_commit_message: Fake commit message
          action_commit_sha: b32575bd5911897df114137828b4b97b5632f6e9fc82ba37a7d7cd59b44e8173
```
