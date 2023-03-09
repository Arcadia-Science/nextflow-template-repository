# Template repository for creating new Nextflow pipelines

This GitHub [template repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/creating-a-repository-from-a-template) can be used to create a new repository with the skeleton of a [Nextflow](https://www.nextflow.io/) pipeline, based on the [nextflow-template](https://github.com/Arcadia-Science/nextflow-template) cookiecutter repository.

## Credit

This is fully inspired by the following blog post: https://simonwillison.net/2021/Aug/28/dynamic-github-repository-templates/. The README instructions here are modified from [this GitHub repository](https://github.com/simonw/click-app-template-repository).

## Usage

You can start [here](https://github.com/Arcadia-Science/nextflow-template-repository/generate) and follow the prompts. Alternatively, you can click on the "Use this template" button on this repository and follow the prompts.

![Example usage when using the template](./template.png)

- The name of your repository will be the name of the Nextflow pipeline.
- Add a one-line description of your pipeline, then click "Create repository from template".
- Make sure to check "Include all branches". This will make following the `nf-core` guidelines easier.

Once created, your new repository will execute a GitHub Actions workflow that uses cookiecutter to rewrite the repository to the desired state. This may take 30 seconds or so. Once the action is done, please rename the `github` directory to `.github`. This is a short-term hack to circumvent GitHub action permission issues.

## Common issues

Depending on the workflow permissions for GitHub actions on your new repository, the setup may fail. To fix, please go to Settings > Actions > General on your new repo. Scroll to the bottom of the page, choose "Read and write permissions" under the "Workflow permissions" section, and hit "Save". Once you retry the action, the setup should work. This setting is easy to configure as default for organizations, but sadly not for individuals.

![Correct workflow permissions for GitHub actions](./permissions.png)
