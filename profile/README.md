# Welcome to the IT Community Github Organization

This Org is managed by Devex, we can be reached at devex@umn.edu or #github / #t3-devx slack channels in the IT@UMN Slack space.  This space is for use by IT Administrative units.

## Community Guidelines

Here are a list of Guidelines for use:
- This community is a place we can put code we'd like to share between teams. 
- Any Repository that has not received any updates in one year will marked as Archived and put into a read-only state.
  - Any Repository that is Archived will get an email sent out to users who have contributed to the repository as notice.
  - Each Repository may also contain a `stakeholders.txt` file in the root that contains email addresses of anyone who relies on the contents of the repository but has not contributed.  This list will also get an email notice.
- Any Repository that has been in an Archived state and not attested to for 1 year will be Deleted.
  - Prior to deletion, an email notification will go out to contributors and stakeholders one week before deletion.

## Code Security Guidelines

- For GitHub Actions, use a full SHA for the version, along with the corresponding version number in the standard Dependabot format (e.g., `actions/checkout@9c091bb21b7c1c1d1991bb908d89e4e9dddfe3e0 # v7.0.0`). This helps mitigate the risk of supply chain attacks.
- A dependabot.yml file should be used to keep dependencies up to date. A cooldown period should also be considered to help mitigate supply chain attack risks.

```
version: 2
updates:
  - package-ecosystem: 'github-actions'
    directory: '/'
    schedule:
      interval: 'weekly'
    cooldown:
      default-days: 7
```

- Consider using a [CODEOWNERS](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners) file to define who will be maintaining the code and ensure the appropriate people are notified of Dependabot pull requests.
