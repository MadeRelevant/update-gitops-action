# GitOps action for updating a gitops repository

This action updates a gitops repository with the latest version of the application.
Example usage:

```yaml
steps:
- name: Update GitOps Repository
  uses: maderelevant/update-gitops-action@master
  with:
    ssh-key: ${{ secrets.SECRET_WITH_SSH_KEY }}
    gitops-repo: your-org/app-gitops
    commit-email: "gitops@your-org.com"
    commit-name: "GitOps"
    changes-by-file: |
      {"path/to/file.yaml" : {
        "serviceA.image": "${{ inputs.yourImage }}",
        "serviceB.image": "${{ inputs.your2ndImage }}"
      }}
```
