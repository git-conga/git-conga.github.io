---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Home
nav-order: 0
---

## Summary

All commit messages must be of the general format:
    
    <type>: <description>

`<type>`: one of `fix`, `feat`, `build`, `ci`, `docs`, `style`, `refactor`, `perf`, or `test`  
`<description>`: a plain-text message.

## Introduction

Git commit messages, like the comments that we _should_ be adding to our code, are means of putting the abstract and conceptual into easily relatable words. A good commit log will allow you to understand the intentions behind you or someone else's code, potentially enabling you to successfully complete a hot-fix to production code at an inconvenient hour of the night.

> Commit-It-Simple is a simple tool to clarify the thoughts and intentions of a software programmer. It is designed to be **useful**, **simple**, and **beautiful**. In that order.

Writing good software is hard. Engineering is a creative endeavour at its heart. Like a beautifully created artwork, the end result should bring joy to its beholder. Simpler is almost always better.

## Version Control

Integrating well-formed commit messages with [Semantic Versioning](https://semver.org/) version numbers allows the messages in your git log to specify your next version.

For a version number [MAJOR.MINOR.PATCH](https://semver.org/#summary), increment:
- MAJOR when incompatible or breaking changes are made
- MINOR when backwards compatible features are added
- PATCH when backwards compatible fixes are made

By flagging changes in commit messages as breaking, a feature, or a fix, it becomes easy for an automated tool to suggest the next version number to be released. Less work for the developer, better version control for the user - a win-win situation. The programmer is now freed up to perform more important tasks.

## Full Specification

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

Commit-It-Simple messages SHALL be written in the format below:

    [![ ]|breaking ]<type>[[ ](<scope>)][[ ]!]:[ ]<description>

    [<body>]

Where angled brackets `<>` denotes a parameter name, text surrounded by square brackets `[]` is OPTIONAL, and pipe `|` denotes multiple valid options.

### 1. Characters

`<type>` MUST consist of only ASCII alphanumeric characters and hypens [0-9A-Za-z-]  
`<scope>` MUST consist of only ASCII alphanumeric characters, hypens, or dots [0-9A-Za-z-.]  
`<description>` MUST consist of any 'normal' ASCII character barring new-lines  
`<body>` MUST consist of any 'normal' ASCII character barring control characters

### 2. Breaking

> BREAKING fix: replace hovercraft's doors with windows

Life is hard, changes can be tough, sometimes to move forward one must break with the past. This has can have negative consequences but these can be greatly reduced if you know what the consequences are and how to work around them.

If you've made a change that breaks an external piece of code, a physical resource, or a human-machine interaction, flag it with the keyword `breaking` so that others are aware of the change. Alternatively, add an exclamation mark before or after the `<type>`. Make sure to adequately document the alteration in the `<description>` and provide advice on other systems can adapt to the breaking change.

### 3. Type

> docs: update loading instructions in readme

The `<type>` describes the nature of the commit, and is one of the two compulsory parameters.
It is RECOMMENDED to be one of:

* `build`
* `ci`
* `docs`
* `feat`
* `fix`
* `perf`
* `refactor`
* `style`
* `test`

The types above are explained in the blog post [Understanding Semantic Commit Messages Using Git and Angular](https://nitayneeman.com/posts/understanding-semantic-commit-messages-using-git-and-angular/#common-types).

Other types may be used instead, particularly for projects that are not of a programming nature, eg: books, documents, Latex reports, system-definitions, use-your-imagination. What is suggested, is that the list of types cover a wide range of functional aspects of the project and are limited to a maximum of ten for appropriate re-usability within a project.

Creators of tools based on Commit-It-Simple SHOULD take the fallibility of humans into account. As such, variations on the spellings of types like `feat`, `feature`, and `features`, or `doc`, and `docs` SHOULD be treated as being equal. Be slow to anger and quick to forgive.

### 4. Scope

> test (hovercraft): check the maximum loading weight

Denoting the `<scope>` of a change is OPTIONAL, but can be a useful method of grouping commits that alter a common piece of code. A module, file, or folder name is often appropriate.

### 5. Description

> feat: teach eels Hungarian

A one-liner that provides a brief overview of the change that has been made. Keep it short and to the point. Start the `<description>` by using a doing-word. See what I did there? Like that.

### 6. Body

> build: load the eels into the hovercraft
>
> I would like some matches for cigarettes

This is the body of the commit message and where all the important details live. Remember, _what_ you've changed is already part of the commit, what other developers (and future you) need to know is _why_ you made the change, or made the change in the way you did.

### 7. Whitespace

The inclusion of spaces within the first line is OPTIONAL, however a space SHOULD be included after the first colon to improve readability.

### 8. Capitalisation

> style: My hovercraft is full of Eels

While sticking to lowercase avoids confusion, sometimes capital letters are required. The important part is to keep it consistent within a repository. Remember: useful, simple, beautiful.

## More Complex Examples

All of the examples below are acceptable Commit-It-Simple commit message formats:

**The simplest message:**

style: isn't it neat

**Defining scope:**

docs(gadgets): remember the gizmos

**Signaling a breaking change**

breaking feat: add the whozits

**Defining scope, including a space:**

fix (whatsits): repair the thingamabobs

**Multiple lines:**

test: How many have I got?  
  
I've got twenty  
But who cares?  
  
I want more

## Inspired by

* [SemVer](https://semver.org/)
* [Angular Commit Message Format](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit)
* [Auto Changelog](https://github.com/Michael-F-Bryan/auto-changelog)
* [Understanding Semantic Commit Messages Using Git and Angular](https://nitayneeman.com/posts/understanding-semantic-commit-messages-using-git-and-angular/)
* [git_commits.py](https://gist.github.com/simonw/091b765a071d1558464371042db3b959#file-get_commits-py)
<!-- * [Commit Message Emoji](https://github.com/dannyfritz/commit-message-emoji) -->
