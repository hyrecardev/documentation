---
description: >-
  This article goes into detail on what inspired Rohit and Raj to choose the
  monorepo paradigm over the traditional monolith
---

# Motivation

## Simplified organization

With multiple repos, you typically either have one project per repo, or an umbrella of related projects per repo, but that forces you to define what a “project” is for your particular team or company, and it sometimes forces you to split and merge repos for reasons that are pure overhead. For example, having to split a project because it's too big or has too much history for your VCS is not optimal.

With a monorepo, projects can be organized and grouped together in whatever way you find to be most logically consistent, and not just because your version control system forces you to organize things in a particular way. Using a single repo also reduces overhead from managing dependencies.

## Simplified dependencies

This probably goes without saying, but with multiple repos, you need to have some way of specifying and versioning dependencies between them. That sounds like it ought to be straightforward, but in practice, most solutions are cumbersome and involve a lot of overhead.

With a monorepo, it's easy to have one universal version number for all projects. Since atomic cross-project commits are possible, the repository can always be in a consistent state -- at commit \#X, all project builds should work. 

## Tooling

The simplification of navigation and dependencies makes it much easier to write tools. Instead of having tools that must understand relationships between repositories, as well as the nature of files within repositories, tools basically just need to be able to read files \(including some file format that specifies dependencies between units within the repo\).

## Cross-project changes

With lots of repos, making cross-repo changes is painful. It typically involves tedious manual coordination across each repo or hack-y scripts. And even if the scripts work, there's the overhead of correctly updating cross-repo version dependencies. Refactoring an API that's used across tens of active internal projects will probably a good chunk of a day. Refactoring an API that's used across thousands of active internal projects is hopeless.

With a monorepo, you just [refactor the API and all of its callers](http://research.google.com/pubs/pub41342.html) in one commit. That's not always trivial, but it's much easier than it would be with lots of small repos. I've seen APIs with thousands of usages across hundreds of projects get refactored and with a monorepo setup it's so easy that it's no one even thinks twice.  


## Downsides

Of course, there are downsides to using a monorepo. I'm not going to discuss them because the downsides are already widely discussed. Monorepos aren't strictly superior to manyrepos. They're not strictly worse, either. My point isn't that you should definitely switch to a monorepo; it's merely that using a monorepo isn't totally unreasonable, that folks at places like Google, Facebook, Twitter, Digital Ocean, and Etsy might have good reasons for preferring a monorepo over hundreds or thousands or tens of thousands of smaller repos.

## 

