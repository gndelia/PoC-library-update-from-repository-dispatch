# PoC-library-update-from-repository-dispatch
PoC about updating a specific library in `package.json` in the context of a github action. This action will be triggered by an event dispatch from the targeted library

### Steps to use

1. install yarn

```
npm install -g yarn
```

1. Install dependencies by running `yarn`

1. Create a personal access token with the repo scope at https://github.com/settings/tokens/new?scopes=repo

1. Set the `GITHUB_TOKEN` env variable with your personal token and run the following command

```
GITHUB_TOKEN=<your-token> node .github/actions/update-library/index.js

```

This Repo is just a PoC to automatically update the version of an internal library. If you want to use it on your own, you need to update the `owner` and `repo` used in `.github/actions/update-library/index.js`

This repository mimics the structure used in the project I work for, and therefore should not be considered as a recommendation.