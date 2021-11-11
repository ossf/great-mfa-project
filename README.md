# The Great MFA Distribution Project

Welcome to the Great MFA Distribution Project
(`great-mfa-project`).
The goal of this project is to:

1. Distribute multi-factor authentication (MFA) tokens to
   some developers of critical open source software (OSS), and
2. Provide or point to information so help people *easily* use MFA tokens.

We have received offers to provide and distribute MFA tokens from
Google and GitHub - thank you so much!

We are currently in the process of creating a plan to do this.
You can see the draft document
[*The Great MFA Distribution Plan*](https://docs.google.com/document/d/1Hhg4KcLCzEdd9ZcbdEviN0TIUTLyWDsIdF6B_hY3Xv0/edit) if you want to see more.
We're doing this carefully, because our goal is *not* turn this
into the "world's best supply chain attack".
We also want to ensure this isn't just a "token effort".

Here are a few key parts of the current plan:

1. Developers who receive MFA tokens through this program will receive
   single-use coupon codes. They'll then to to a site clearly controlled
   by a donator (e.g., *.google.com or *.github.com), and then
   supply information such as their name and coupon code.
2. We need to be able to show that we're helping (metrics).
3. We need to provide or link to information to make these easy to use
   for common cases.

Why do this? Our goal is to prevent supply chain attacks involving
weak or compromised credentials of developers of open source software.
The
["Backstabber's Knife Collection: A Review of Open Source Software Supply Chain Attack" by Ohm et al](https://arxiv.org/abs/2005.09535)
noted that this is one way to subvert OSS, e.g.,
its source code (in a force) or its package (in a package repository).
Here are examples:

* coa and rc - ["Malware found in coa and rc, two npm packages with 23M weekly downloads", 2021-11-05](https://therecord.media/malware-found-in-coa-and-rc-two-npm-packages-with-23m-weekly-downloads/)
* UA-Parser-JS library;  - ["Popular NPM package UA-Parser-JS poisoned with cryptomining, password-stealing malware", Adam Bannister, 2021-10-25](https://portswigger.net/daily-swig/popular-npm-package-ua-parser-js-poisoned-with-cryptomining-password-stealing-malware)
* Homebrew - [Holmes, E.: "How i gained commit access to homebrew in 30 minutes", 2018](https://medium.com/@vesirin/how-i-gained-commit-access-to-homebrew-in-30-minutes-2ae314df03ab)
* Gentoo Linux - [Khandelwal, S. "Password-guessing was used to hack gentoo linux github account", 2017]( https://thehackernews.com/2018/07/github-hacking-gentoo-linux.html)

MFA tokens don't counter all attacks (such as typosquatting)
but they can definitely help.

Some will refer to these as "two-factor authentication" (2FA) tokens,
however, for various reasons we're using the term "MFA" instead.

The Great MFA Distribution Project is a project of the Linux Foundation's
[Open Source Security Foundation (OpenSSF)](https://openssf.org/)
within its
[Best Practices Working Group](https://github.com/ossf/wg-best-practices-os-developers).
Discussions are held within that working group's
mailing list and online meetings.

All documents, including any improvements, are released under the
[Creative Commons Attribution (CC BY) license](https://creativecommons.org/licenses/by/4.0/).
