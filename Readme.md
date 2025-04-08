# Usage from Any Repo
# .github/workflows/reusable-deploy.yml

name: Reuse DevOps Workflow

on:
  push:
    branches:
      - main
      - develop
      - 'feature/**'

jobs:
  call-devops-repo:
    uses: WEBFORX/connect-reusable-workflow/.github/workflows/reusable-deploy.yml@main
    secrets:
      GIT_CLONE_USER: ${{ secrets.GIT_CLONE_USER }}
      GIT_CLONE_TOKEN: ${{ secrets.GIT_CLONE_TOKEN }}
      


# Usage Guide

## ✅ Summary

| Action                         | How                                       |
|-------------------------------|-------------------------------------------|
| **Public Access**             | Repo Settings → Change to Public          |
| **Versioning**                | Use Git tags like `v1.0.0`, `v1`, etc.    |
| **Stability for Consumers**   | Reference tags instead of `main`          |


