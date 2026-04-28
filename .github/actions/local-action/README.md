# Local Action

<!-- about this action -->

| Input   | Description                                                                                                 | Required |
| ------- | ----------------------------------------------------------------------------------------------------------- | -------- |
| `token` | Token used to access the GitHub API. Use the `GITHUB_TOKEN` by default unless other permissions are needed. | yes      |

## What checks does this action conduct?

- Validates repository configuration using the GitHub API
- Checks whether required workflow files (such as CodeQL configuration) exist
- Verifies that workflow triggers (e.g., pull_request) are correctly defined
- Ensures required inputs (such as token) are provided
- Confirms that the repository meets the expected exercise or workflow requirements

## What about this action is sensitive or might raise security concerns?

This action uses a GitHub token (`GITHUB_TOKEN`) to interact with the GitHub API.

This is sensitive because the token provides access to repository resources, including reading contents and writing security-related data. If the token is exposed or misused, it could allow unauthorized access or modifications.

Additionally, using untrusted actions or granting excessive permissions may increase security risks. It is important to follow the principle of least privilege and use only trusted actions.

## Summary

This action performs automated checks on repository configuration and workflows using the GitHub API. It relies on a token for authentication, which introduces security considerations if not properly managed. Proper permission control and trusted usage are essential.
