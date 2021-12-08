# The Great MFA Distribution Project

Welcome to the Great MFA Distribution Project
(`great-mfa-project`).
The goal of this project is to:

1. Promote the use of multi-factor authentications through out all stages of Open Source Software (OSS) development
2. Distribute multi-factor authentication (MFA) tokens to
   some developers of critical open source software, and
2. Provide or point to information so help people *easily* use MFA tokens.

The OpenSSF is working with Google and GitHub who have generously offered to provide and distribute MFA tokens.
Thank you!

MFA tokens, also called keys, are hardware devices specifically for authentication.
These MFA tokens can be used in many applications in a developers workflow.  They help provide higher degrees
of validation for a developer's identity when logging into code repositories or applications, or performing 
critical tasks such as signing code.

## How do I get an MFA token?

If your open source software (OSS) project has notified you that
you're getting a free token from us,
you'll receive a Google coupon code or a GitHub validation code.
Here are step-by-step instructions:

* [How to get a Titan token from Google](getting-titan-token-from-google.md)
* [How to get a Yubikey token from GitHub](getting-yubikey-token-from-github.md)

If you contribute to an OSS project and were not contacted during our first round of
token distribution, please reach out to our [Working Group](openssf-wg-best-practices+owner@lists.openssf.org) for more information.

The OpenSSF cares about privacy and does *not* get detailed lists of
who gets every token; we only get aggregate values (per-project Google tokens
and aggregate totals from GitHub).

## How do I use an MFA token?

For some simple instructions on how to use MFA tokens for common OSS
situations see our [Token Usage Guide](guide/token-usage-guide.md).

## How we're doing this

Here is our basic plan:
* Create a list of about 100 critical open source software (OSS) projects.
  This was determined by the [OpenSSF Securing Critical Projects Working Group](https://github.com/ossf/wg-securing-critical-projects).
  [Here is the list of critical OSS projects and who will be notifying them from the Great MFA Distribution Project](https://docs.google.com/spreadsheets/d/1sO_tJ_B7_2I-TUx23pnBoIRJIqaOm8yBnKAwqs7DwBw/edit#gid=0).
  The list of projects is the same as the list of
  [critical OSS projects identified by the critical projects WG by 2021-12-02](https://docs.google.com/spreadsheets/d/1ONZ4qeMq8xmeCHX03lIgIYE4MEXVfVL6oj05lbuXTDM/edit#gid=0). We're currently using the version as of
  2021-12-02, because the Google coupon codes expire on 2021-12-31.
* Develop a set of simple documents on how to use these tokens
  for common OSS cases. First drafts were done 2021-12-02, but we'll
  keep refining them.
* Send an [invitation](./invitation.txt) to each critical OSS project. This will be done by one of the great-mfa-plan notifiers, typically by filing an issue, in 2021-12-02..09.
  The current Great MFA Distribution Project notifiers are
  David A. Wheeler (Linux Foundation), Xavier Rene-Corail (GitHub),
  Jose Palafox (GitHub), Marta Rybczynska (Syslinbit),
  CRob (@SecurityRob) (Intel), John Naulty (Coinbase),
  Arnaud J Le Hors (IBM), Glenn ten Cate (OWASP), and
  Georg Kunz (Ericsson).
  Note: Organizational affiliations are *only* shown to clarify who we mean.
* If a project accepts, the notifier will tell a sender (David A. Wheeler or Jory Burson) key information: the project who has accepted, the email address to send private information to, and how the project accepted. The sender will then send the project the coupon codes and validation codes using the [coupon_sending.md](./coupon_sending.md) template. This is 2021-12-03..31.
* Projects distribute the codes. Receivers use them to get the tokens from
  the Google Store or GitHub shop. Then the tokens get used!
* Projects send back some information, that we combine with other data
  and determine whether or not we've had a positive effect (hopefully we have!).

You can see the draft document
[*The Great MFA Distribution Plan*](https://docs.google.com/document/d/1Hhg4KcLCzEdd9ZcbdEviN0TIUTLyWDsIdF6B_hY3Xv0/edit) if you want to see more detail.
We've taken some steps to make sure this does *not* turn into
the "world's best supply chain attack"; see our
[security rationale](./security-rationale.md).
We also want to ensure this isn't just a "token effort".


## Why are we doing this?

Why do this? Our goal is to prevent supply chain attacks involving
weak or compromised credentials of developers of open source software.

Over the last several years Open Source Software has become critical upstream components 
of many aspects of software and applications that are used the world-over.  Along with this
increase in use, so has the potential for malicious actors to exploit the amazing work OSS
communities develop each day.  

The
["Backstabber's Knife Collection: A Review of Open Source Software Supply Chain Attack" by Ohm et al](https://arxiv.org/abs/2005.09535)
noted that this is one way to subvert OSS, e.g.,
its source code (in a force) or its package (in a package repository).
Here are examples:

* coa and rc - ["Malware found in coa and rc, two npm packages with 23M weekly downloads", 2021-11-05](https://therecord.media/malware-found-in-coa-and-rc-two-npm-packages-with-23m-weekly-downloads/)
* UA-Parser-JS library;  - ["Popular NPM package UA-Parser-JS poisoned with cryptomining, password-stealing malware", Adam Bannister, 2021-10-25](https://portswigger.net/daily-swig/popular-npm-package-ua-parser-js-poisoned-with-cryptomining-password-stealing-malware)
* Homebrew - [Holmes, E.: "How i gained commit access to homebrew in 30 minutes", 2018](https://medium.com/@vesirin/how-i-gained-commit-access-to-homebrew-in-30-minutes-2ae314df03ab)
* Gentoo Linux - [Khandelwal, S. "Password-guessing was used to hack gentoo linux github account", 2017]( https://thehackernews.com/2018/07/github-hacking-gentoo-linux.html)

MFA tokens don't counter all attacks (such as typosquatting). Also the hardware tokens should not be left unguarded in untrusted spaces as there are known [side-channel attacks](https://www.zdnet.com/article/new-side-channel-attack-can-recover-encryption-keys-from-google-titan-security-keys/) existing against hardware tokens. 
By using tools such as Multi-factor Authentication, the likelihood that such bad actors would be able to violate the integrity of that open source supply chain is greatly reduced.

This will increase the level of security and protection for your project immensely but use your common sense. 

## Background information

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
