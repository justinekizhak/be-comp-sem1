# Contributing <!-- omit in toc -->

## Table of contents <!-- omit in toc -->

- [First things first](#first-things-first)
    - [For terminal wizards](#for-terminal-wizards)
    - [For people who likes to click stuffs](#for-people-who-likes-to-click-stuffs)
- [Branches](#branches)
- [Commit messages](#commit-messages)
- [Tagging](#tagging)
- [Merge Request Process](#merge-request-process)
- [Need some help?](#need-some-help)
    - [Using terminal?](#using-terminal)
    - [GUI lovers?](#gui-lovers)
- [Creating a new Issue](#creating-a-new-issue)
    - [Labelling method](#labelling-method)

You are here to help? Awesome, feel welcome and read the following sections
in order to know how to ask questions and how to work on something.

All members of our community are expected to follow our [Code of Conduct].
Please make sure you are welcoming and friendly in all of our spaces.

Get in touch with the members of the community.  
Report bugs, suggest features or view the source code on GitHub.  
And mostly have fun!

If you are new to contributing then please start with "Issues" available on the
website.

[Code of Conduct]: CODE_OF_CONDUCT.md

## First things first

We use [Git flow] branching method.
So get familiar with it.

[Git flow]: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

### For terminal wizards

Personally this is the best way ever. No need to lift your hand from the
keyboard.  
But beware if you are not comfortable with terminal and a keyboard.

For macOS users `brew install git-flow` should work, provided you have [Homebrew]
installed.  
And for Linux users `apt-get install git-flow`.

*For more instructions on installing gitflow [read this].  
Install [Homebrew].*

[Homebrew]: https://brew.sh
[read this]: https://github.com/nvie/gitflow

### For people who likes to click stuffs

Install [Sourcetree], or [GitKraken]. Both are good. Sourcetree feels faster,
but Kraken has cooler UI.

Read [how to git-flow using sourcetree].

[Sourcetree]: https://www.sourcetreeapp.com
[GitKraken]: https://www.gitkraken.com
[how to git-flow using sourcetree]: https://medium.com/@budioktaviyans/how-to-make-a-git-flow-using-sourcetree-20ab77fe6813

## Branches

There are two permanent branches.

1. `master`. This branch is the most stable production one.

2. `develop`. This branch is where actual development takes place.

## Commit messages

Please read [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/).

Basically follow these 7 rules:

1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

## Tagging

All tags start with `v`.
Examples: `v3.2.1`.

The versioning scheme we use is [SemVer](http://semver.org/).

## Merge Request Process

1. Ensure that no build files are uploaded.
2. Update the README with details of changes to the interface, this includes
    new environment variables, exposed ports, useful file locations and container
    parameters.
3. Bump up the version numbers in any examples files and the README.md to the
    new version that this merge request would represent.
4. All Merge Request needs to be labeled appropriately. Check [Labelling method].
5. Please use the Merge Request template to maintain consistency.

## Need some help?

### Using terminal?

Great. First run `git flow init` in your project root.

Then accept all the defaults:

``` bash
Branch name for production releases: [master]
Branch name for "next release" development: [develop]
Feature branches: [feature/]
Release branches: [release/]
Hotfix branches: [hotfix/]
Support branches: [support/]
Version tag prefix: []
```

Instructions to use git-flow:

1. Creating a feature branch
    ``` bash
    git flow feature start feature_branch
    ```

2. Finishing a feature branch
    ```bash
    git flow feature finish feature_branch
    ```

3. Creating a release branch
    ``` bash
    git flow release start 0.1.0
    ```

4. Merging a release branch into master and develop
    ``` bash
    git checkout master
    git checkout merge release/0.1.0
    git flow release finish '0.1.0'
    ```

5. Creating a hotfix branch
    ``` bash
    git flow hotfix start hotfix_branch
    ```

6. Finishing a hotfix branch
    ``` bash
    git flow hotfix finish hotfix_branch
    ```

### GUI lovers?

Just make sure the above defaults are used.

## Creating a new Issue

Please use issues as much as possible. Issues are the best way to communicate
about the project. Don't email the project maintainers unless necessary.

Please use the template. Every issue must have correct labels, milestone
information.

For Bug reports one issue per bug. If multiple bugs are related then use related
feature on the website or add the url to the related bug in the Description.

### Labelling method

All issues are categorized into three:

1. **Priority**
    1. ~"Priority: Critical"
    2. ~"Priority: High"
    3. ~"Priority: Medium"
    4. ~"Priority: Low"

2. **Type**
    1. ~"Type: Bug"
    2. ~"Type: Maintenance"
    3. ~"Type: Enhancement"
    4. ~"Type: Discussion"

3. **Status**
    1. ~"Status: To Do"
    2. ~"Status: In Progress"
    3. ~"Status: In Review"

[Labelling method]: (#labelling-method)
