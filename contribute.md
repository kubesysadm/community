
# Welcome to Kubesysadm!

-   [Before you get started](#before-you-get-started)
    -   [Code of Conduct](#code-of-conduct)
    -   [Community Expectations](#community-expectations)
    -   [License Compliance Rules](#license-compliance-rules)
-   [Getting started](#getting-started)
-   [Your First Contribution](#your-first-contribution)
    -   [Find something to work on](#find-something-to-work-on)
        -   [Find a good first topic](#find-a-good-first-topic)
        -   [Work on an Issue](#work-on-an-issue)
        -   [File an Issue](#file-an-issue)
-   [Contributor Workflow](#contributor-workflow)
    -   [Creating Pull Requests](#creating-pull-requests)
    -   [Code Review](#code-review)
    -   [Testing](#testing)

# Before you get started

## Code of Conduct

Please make sure to read and observe our [Code of Conduct](./code_of_conduct.md).

## Community Expectations

Kubesysadm is a community project driven by its community which strives to promote a healthy, friendly and productive environment.
The goal of the community is to develop a kubesysadm system which is useful for managing kubernete's resource. To build a such kubesysadm system at such scale requires the support of a community with similar aspirations.

- See [Community Membership](./community-membership.md) for a list of various community roles. With gradual contributions, one can move up in the chain.

## License Compliance Rules

Please ensure that you have read the [license compliance rules](./compliance.md#rules)

It specifies that licenses listed in the "restrictions" section cannot be used in the kubesysadm project. Licenses in the "reciprocal_licenses" section can be used but modifications are not permitted.

If you need to use a license that is not included in either section, please open a Pull Requests for discussion.

# Getting started

- Read the [get started](https://kubesysadm.sysadm.cn/en/docs/installation/#prerequisites) for developing code for Kubesysadm
- Read the [setup](https://kubesysadm.sysadm.cn/en/docs/installation/#install-from-code) for build/deploy instructions.


# Your First Contribution

We will help you to contribute in different areas like filing issues, developing features, fixing critical bugs and getting your work reviewed and merged.

If you have questions about the development process, feel free to jump into our [Slack Channel](https://kubesysadm.slack.com/) or join our [mailing list](https://groups.google.com/forum/#!forum/kubesysadm).

## Find something to work on

We are always in need of help, be it fixing documentation, reporting bugs or writing some code.
Look at places where you feel best coding practices aren't followed, code refactoring is needed or tests are missing.
Here is how you get started.

### Find a good first topic

There are [multiple repositories](https://github.com/kubesysadm/) within the Kubesysadm organization.
Each repository has beginner-friendly issues that provide a good first issue.

Another good way to contribute is to find a documentation improvement, such as a missing/broken link.

#### Work on an issue

When you are willing to take on an issue, you can assign it to yourself. Just reply with `/assign` or `/assign @yourself` on an issue,
then the robot will assign the issue to you and your name will present at `Assignees` list.

### File an Issue

While we encourage everyone to contribute code, it is also appreciated when someone reports an issue.
Issues should be filed under the appropriate Kubesysadm sub-repository.

*Example:* a Kubesysadm issue should be opened to [Kubesysadm](https://github.com/kubesysadm/kubesysadm/issues).

Please follow the prompted submission guidelines while opening an issue.

# Contributor Workflow

Please do not ever hesitate to ask a question or send a pull request.

This is a rough outline of what a contributor's workflow looks like:

- Create a topic branch from where to base the contribution. This is usually master.
- Make commits of logical units.
- Make sure commit messages are in the proper format (see below).
- Push changes in a topic branch to a personal fork of the repository.
- Submit a pull request to [Kubesysadm](https://github.com/kubesysadm/kubesysadm).
- The PR must receive an approval from two maintainers.

## Creating Pull Requests

Pull requests are often called simply "PR".
Kubesysadm generally follows the standard [github pull request](https://help.github.com/articles/about-pull-requests/) process.

In addition to the above process, a bot will begin applying structured labels to your PR.

The bot may also make some helpful suggestions for commands to run in your PR to facilitate review.
These `/command` options can be entered in comments to trigger auto-labeling and notifications.
Refer to its [command reference documentation](https://go.k8s.io/bot-commands).

## Code Review

To make it easier for your PR to receive reviews, consider the reviewers will need you to:

* follow [good coding guidelines](https://github.com/golang/go/wiki/CodeReviewComments).
* write [good commit messages](https://chris.beams.io/posts/git-commit/).
* break large changes into a logical series of smaller patches which individually make easily understandable changes, and in aggregate solve a broader issue.
* label PRs with appropriate reviewers: to do this read the messages the bot sends you to guide you through the PR process.

### Format of the commit message

We follow a rough convention for commit messages that is designed to answer two questions: what changed and why.
The subject line should feature the what and the body of the commit should describe the why.

```
scripts: add test codes for metamanager

this add some unit test codes to improve code coverage for metamanager

Fixes #12
```

The format can be described more formally as follows:

```
<subsystem>: <what changed>
<BLANK LINE>
<why this change was made>
<BLANK LINE>
<footer>
```

The first line is the subject and should be no longer than 70 characters, the second line is always blank, and other lines should be wrapped at 80 characters. This allows the message to be easier to read on GitHub as well as in various git tools.

Note: if your pull request isn't getting enough attention, you can use the reach out on Slack to get help finding reviewers.

## Testing

There are multiple types of tests.
The location of the test code varies with type, as do the specifics of the environment needed to successfully run the test:

* Unit: These confirm that a particular function behaves as intended. Unit test source code can be found adjacent to the corresponding source code within a given package. These are easily run locally by any developer.
* Integration: These tests cover interactions of package components or interactions between Kubesysadm components and Kubernetes control plane components like API server.
* End-to-end ("e2e"): These are broad tests of overall system behavior and coherence. The e2e tests are in [Kubesysadm e2e](https://github.com/kubesysadm/kubesysadm/tree/main/test/e2e).

Continuous integration will run these tests on PRs.
