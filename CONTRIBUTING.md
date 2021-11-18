# Contributing

## What should I know before I get started?

Please read about the project on the [main page of this repository](https://github.com/IKEA/IKEA3DAssemblyDataset/).

## How to contribute to this project

We would love to know if you find errors to this project.
If you do, create an issue.

## Creating an issue

Creating an issue for errors is an important way you can contribute to the IKEA3DAssemblyDataset.
This section guides you through submitting an issue report regarding the IKEA3DAssemblyDataset. Following these guidelines helps maintainers and the community understand your report, reproduce the behavior, and find related reports. When creating an issue, you will be asked to select and follow one of the repository issues templates, depending on the matter of the issue you want to report.

Before creating an issue, please check that an issue reporting the same problem does not already exist. If there is such an open issue, you may add your information as a comment.

When creating an issue, please include

1. The name of the file that contains the error.
2. Description of the error/fix.
3. Screenshot where you have marked the area that needs to be fixed.
This is especially important when you found an error on a 3D or 2D file.

When you are creating an issue, please include as many details as possible.
Issues are tracked as [GitHub issues](https://guides.github.com/features/issues/).

## Pull requests

We are not accepting pull requests for changed 3D models. The reason is that IKEA need to update the source 3D files at IKEA and generate a new version which is exported either to .glTF or .obj format to add to the repo. Pull requests to change or add 3D models to the repo will only be accepted for review if they are created by the [repository maintainers](https://github.com/IKEA/IKEA3DAssemblyDataset/blob/main/MAINTAINERS.md).

## Participation Guidelines (Code of Conduct)

IKEA have for this repository adopted the [Contributor Covenant](https://www.contributor-covenant.org/) and project participants are expected to adhere to it. Please read the [Participation Guidelines (Code of Conduct)](CODE_OF_CONDUCT.md) to understand what actions will and will not be tolerated. Read more about our [rules for communication](COMMUNICATION.md) here.

## Creating new 3D models *[this is information is for IKEA maintainers]*

### For the .glTF/.glB models

1. Create new 3D models using 3ds Max 2021
2. Make sure you always are using mm as a system unit inside 3ds Max
3. Export the .glTF/.glB models using babylonJs exporter in 3ds Max
4. Remember to add copyright information to the files

### For the .obj models

1. Create new 3D models using 3ds Max 2021
2. Make sure you always are using mm as a system unit inside 3ds Max
3. Export the .obj models using standard 3ds Max
4. Doublecheck that you exported the model with the correct units
5. Remember to add copyright information inside the header of the files

<!--
### DO NOT EDIT
This section describes the process to be followed by IKEA maintainers when a new release or a fix needs to be applied to the dataset.
## Making a pull request
*   Always follow the seven rules of a [great Git commit message](#git-commit-messages)
*   Follow the normal [pull request flow](https://help.github.com/articles/creating-a-pull-request/).
*   Feel free to make as many commits as you want; we will squash them all into a single commit before merging your change.
*   Check the diffs, write a useful description (including something like `Fixes #123` if it's fixing a bug) and send the PR out. Please start the title of your pull request with the name of the affected package, followed
    by a colon, followed by a short summary of the change, like "blob/gcsblob:add more tests".
* There is no need to assign a reviewer to the PR, the project team will assign someone for review during the standard triaging process. OR Choose a reviewer from the maintainers guide.

#### Git Commit Messages
A well-crafted Git commit message is the best way to communicate context about a change to fellow developers (and indeed to their future selves).
Follow the seven rules of a great Git commit message:
* Separate subject from body with a blank line. 
* Limit the subject line to 50 characters.
* Capitalize the subject line.
* Do not end the subject line with a period.
* Use the imperative mood in the subject line. eg."Add feature" not "Added feature"
* Wrap the body at 72 characters.
* Use the body to explain what and why vs. how.

## Code review
All submissions, including submissions by project members, require review. It is almost never the case that a pull request is accepted without some changes requested, so please do not be offended!

When you have finished making requested changes to your pull request, please make a comment containing "PTAL" (Please Take Another Look) on your pull request. GitHub notifications can be noisy, and it is unfortunately easy for things to be lost in the shuffle.

Once your PR is approved (hooray!), the reviewer will squash your commits into a single commit and then merge the commit onto the main branch. Thank you!

## Github code review workflow conventions
(For project members and frequent contributors.)

As a contributor:

-   Try hard to make each Pull Request as small and focused as possible. In
    particular, this means that if a reviewer asks you to do something that is
    beyond the scope of the Pull Request, the best practice is to file another
    issue and reference it from the Pull Request rather than just adding more
    commits to the existing PR.
-   Adding someone as a Reviewer means "please feel free to look and comment". Choose as many Reviewers as you'd like referring the Maintainers.
-   Adding someone as an Assignee means that the Pull Request should not be
    submitted until they approve. If you choose multiple Assignees, wait until
    all of them approve. It is fine to ask someone if they are OK with being
    removed as an Assignee.
-   Make as many commits as you want locally, but try not to push them to Github until you've addressed comments; this allows the email notification about the push to be a signal to reviewers that the PR is ready to be looked at again.
-   When there may be confusion about what should happen next for a PR, be
    explicit; add a "PTAL" comment if it is ready for review again, or a "Please hold off on reviewing for now" if you are still working on addressing comments.
-   "Resolve" comments that you are sure you've addressed; let your reviewers
    resolve ones that you're not sure about.
-   Do not use `git push --force`; this can cause comments from your reviewers
    that are associated with a specific commit to be lost. This implies that
    once you've sent a Pull Request, you should use `git merge` instead of `git rebase` to incorporate commits from the master branch.

As a reviewer:

-   Be timely in your review process, especially if you are an Assignee.
-   Try to use `Start a Review` instead of single comments, to reduce email
    spam.
-   "Resolve" your own comments if they have been addressed.
-   If you want your review to be blocking, and are not currently an Assignee,
    add yourself as an Assignee.

When squashing-and-merging:

-   Ensure that **all** of the Assignees have approved.
-   Do a final review of the one-line PR summary, ensuring that it meets the
    guidelines (e.g., "blob: add more blobbing") and accurately describes the
    change.
-   Delete the automatically added commit lines; these are generally not
    interesting and make commit history harder to read.
-->
