# Rules for AWS S3 Misconfiguration

Try Selefra's pre-written rules for detecting AWS S3 misconfigurations. Before applying rules, read about [project structure](https://selefra.io/docs/project-structure/overview/).  
You can either clone this repo, or if only performing a few specific tasks, download single rule files to project directory.

## Instruction
### Project Structure
At least one project should be created prior to applying rules. A project should comprise following files:
```YAML
├── logs
├── module.yaml
├── rules
│   └── some.yaml
└── selefra.yaml
```
### Steps to Apply Rule
Configure based on your current needs. In this case, infrastructure of interest should be *AWS*:

- [`selefra`](https://selefra.io/docs/project-structure/infrastructure) contains settings for the project and providers' plugins.
- [`providers`](https://selefra.io/docs/project-structure/providers) contains provider credentials and account settings.
- [`rules`](https://selefra.io/docs/project-structure/rules)  contains infrastructure-as-code test items.
- [`modules`](https://selefra.io/docs/project-structure/modules)  contains files and directories containing rules.

Check to see if configuration for **infrastructure**-`selefra.yaml` and **account**-`providers.yaml` are aligned. Go to folder `rules`, add rules in YAML from [this list](https://github.com/selefra/rules-aws-misconfigure-s3/tree/main/rules/s3). Open `modules.yaml`, make sure correct folder is being directed in `uses: path/to/rule`. To apply the rule, run CLI command [`selefra apply`](https://selefra.io/docs/selefra-cli/create-project/#apply).

## Documentation

See [Docs](https://selefra.io/docs) for best practices and detailed instructions. In docs, you will find info on installation, CLI usage, project workflow and more guides on how to accomplish cloud inspection tasks.

## Community

Selefra is a community-driven project, we welcome you to open a [GitHub Issue](https://github.com/selefra/selefra/issues/new/choose) to report a bug, suggest an improvement, or request new feature.

-  Join [Selefra Community](https://selefra.slack.com) on Slack. We host `Community Hour` for tutorials and Q&As on regular basis.
-  Follow us on [Twitter](https://twitter.com/SelefraCorp) and share your thoughts！

## CONTRIBUTING

For developers interested in building Selefra codebase, read through [Contributing.md](https://github.com/selefra/selefra/blob/main/CONTRIBUTING.md) and [Selefra Roadmap](https://github.com/orgs/selefra/projects/1). 
Let us know what you would like to work on!

## License

[Mozilla Public License v2.0](https://github.com/selefra/selefra/blob/main/LICENSE)
