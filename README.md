# The Great MFA Distribution Project

Welcome to the Great MFA Distribution Project
(`great-mfa-project`).
The goal of this project is to:

1. Promote the use of multi-factor authentication (MFA) through out all stages of Open Source Software (OSS) development
2. Distribute MFA tokens to some developers of critical OSS, and
3. Provide or point to information to help people *easily* use MFA tokens.

The OpenSSF is working with Google and GitHub who have generously offered to provide and distribute MFA tokens.
Thank you!

MFA tokens, also called keys or fobs, are hardware devices specifically for authentication.
These MFA tokens can be used in many applications in a developer's workflow.  They help provide higher degrees
of validation for a developer's identity when logging into code repositories or applications, or performing 
critical tasks such as signing code.
Attackers generally find it much harder to take over an account authenticated with an MFA token compared to an account authenticated with only a password;
see [why we are doing this](#why-we-ard-doing-this) for more information.

## How do I get an MFA token?

If your open source software (OSS) project has been notified that
you're getting a free token from us,
you'll receive a Google coupon code or a GitHub validation code.
Here are step-by-step instructions:

* [How to get a Titan token from Google](getting-titan-token-from-google.md)
* [How to get a Yubikey token from GitHub](getting-yubikey-token-from-github.md)

If you contribute to an OSS project and were not contacted during our first round of
token distribution, please reach out to our [Working Group](mailto:openssf-wg-best-practices+owner@lists.openssf.org) for more information.

The OpenSSF cares about privacy and does *not* get detailed lists of
who gets every token; we only get aggregate values (per-project Google tokens
and aggregate totals from GitHub).

## How do I use an MFA token?

For some simple instructions on how to use MFA tokens for common OSS
situations see our [Token Usage Guide](guide/token-usage-guide.md).

## How we're doing this

Here is our basic plan:
* Create a list of about 100 critical open source software (OSS) projects.
  [Here is the list of critical OSS projects and who will be notifying them from the Great MFA Distribution Project](https://docs.google.com/spreadsheets/d/1sO_tJ_B7_2I-TUx23pnBoIRJIqaOm8yBnKAwqs7DwBw/edit#gid=0).
  For more information, see the section below on
  [how this collection of critical OSS projects were selected](#how-were-critical-oss-projects-selected).
* Develop a set of simple documents on how to use these tokens
  for common OSS cases. First drafts were done 2021-12-02, but we'll
  keep refining them.
* Send an [invitation](./invitation.txt) to each critical OSS project. This will be done by one of the great-mfa-plan notifiers, typically by filing an issue, in 2021-12-02..10. The current Great MFA Distribution Project notifiers, with GitHub/GitLab account names and organizational affiliations, are:
  - David A. Wheeler (@david-a-wheeler/@david-a-wheeler) (Linux Foundation),
  - CRob (@SecurityRob) (Intel),
  - Xavier Rene-Corail (@xcorail) (GitHub),
  - John Naulty (@jnaulty) (Coinbase),
  - Jose Palafox (@josepalafox) (GitHub),
  - Marta Rybczynska (Syslinbit),
  - Arnaud J Le Hors (@lehors) (IBM),
  - Glenn ten Cate (@blabla1337) (OWASP),
  - Georg Kunz (@gkunz) (Ericsson), and
  - Jory Burson (@jorydotcom) (Linux Foundation).
* If a project accepts, the notifier will tell a sender (David A. Wheeler or Jory Burson) key information: the project who has accepted, the email address to send private information to, and how the project accepted. The sender will then send the project the coupon codes and validation codes using the [coupon_sending.md](./coupon_sending.md) template. This is 2021-12-03..31.
* Projects distribute the codes. Receivers use them to get the tokens from
  the Google Store or GitHub shop. Then the tokens get used!
* Projects send back some information, that we combine with other data
  and determine whether or not we've had a positive effect (hopefully we have!).

Note: Organizational affiliations are *only* shown to clarify who we mean.

We've taken some steps to make sure this does *not* turn into
the "world's best supply chain attack". See our
[security rationale](./security-rationale.md).
We also want to ensure this isn't just a "token effort".
You can see the now-obsolete draft document
[*The Great MFA Distribution Plan*](https://docs.google.com/document/d/1Hhg4KcLCzEdd9ZcbdEviN0TIUTLyWDsIdF6B_hY3Xv0/edit) if you want to see more detail.


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
its source code (in a forge) or its package (in a package repository).
Here are examples:

* coa and rc - ["Malware found in coa and rc, two npm packages with 23M weekly downloads", 2021-11-05](https://therecord.media/malware-found-in-coa-and-rc-two-npm-packages-with-23m-weekly-downloads/)
* UA-Parser-JS library;  - ["Popular NPM package UA-Parser-JS poisoned with cryptomining, password-stealing malware", Adam Bannister, 2021-10-25](https://portswigger.net/daily-swig/popular-npm-package-ua-parser-js-poisoned-with-cryptomining-password-stealing-malware)
* Homebrew - [Holmes, E.: "How i gained commit access to homebrew in 30 minutes", 2018](https://medium.com/@vesirin/how-i-gained-commit-access-to-homebrew-in-30-minutes-2ae314df03ab)
* Gentoo Linux - [Khandelwal, S. "Password-guessing was used to hack gentoo linux github account", 2017]( https://thehackernews.com/2018/07/github-hacking-gentoo-linux.html)

MFA tokens don't counter all attacks (such as typosquatting). Also the hardware tokens should not be left unguarded in untrusted spaces as there are known [side-channel attacks](https://www.zdnet.com/article/new-side-channel-attack-can-recover-encryption-keys-from-google-titan-security-keys/) existing against hardware tokens. 
Still, by using tools such as Multi-factor Authentication, the likelihood that bad actors will be able to violate the integrity of that open source supply chain is greatly reduced.

This will increase the level of security and protection for your project immensely, but use your common sense. 

## How were critical OSS projects selected?

For our purposes, a critical OSS project is an OSS project that can have
an especially large impact if it has a significant unintentional vulnerability,
or if it is subverted in either its source repository or
distribution package(s).
There are literally millions of open source software (OSS) projects today,
making it difficult to create a focused list of "critical OSS projects".

The list of critical OSS projects was developed for the Great MFA Distribution
Project by the
[OpenSSF Securing Critical Projects Working Group (WG)](https://github.com/ossf/wg-securing-critical-projects).
This OpenSSF working group has been *specifically* working on this problem!

There are many ways to identify "critical" projects, so the
Securing Critical Projects WG combined the results of several different
analyses (the analyses are also called "Selection Criteria"),
The WG then used human group review of this combined set of top candidates
to create a final defensible list. The analyses ("selection criteria") for
identifying candidate critical OSS projects included:

* [OpenSSF Criticality Score](https://github.com/ossf/criticality_score): A top OpenSSF criticality score value. This metric prefers projects that are extremely active on specific forges. Such projects are likely to be important (at least to the participants). However, this is not a perfect measure; some projects will score low here and yet be very critical. Also, it currently only considers GitHub-hosted projects. As of 2021-11-23 the projects with the top scores are node, kubernetes, rust, and spark.
* [Census Program II](https://www.coreinfrastructure.org/programs/census-program-ii/): Harvard preliminary analysis, uses SCA & dependency data. This tends to emphasize lower-level libraries that are depended on, transitively, by many.
* OSTIF Managed Audit Program: Programs OSTIF has recommended for audit. These were selected earlier from research sources, focusing on securing the most critical projects. You can see the [OSTIF Managed Audit Program (MAP25)](https://docs.google.com/spreadsheets/d/1oytKuD7UCX6nDXWQMr6ZgYYgap_SH_JVBof5gNrgSxo/edit#gid=0)
* [Top Google Project](https://opensource.google/projects/list/featured):	Featured on Google Open Source page and widely adopted.
* [Top Microsoft Project](https://opensource.microsoft.com/projects/): Featured on Microsoft Open Source page and widely adopted.
* [Top Linux Foundation Project](https://www.linuxfoundation.org/projects/): 	Featured on Linux Foundation Project page and related to supply chains.
*  Secure Supply Chain Tool: Directly related to supply chain security (identified by WG)
* Survey Response: [Response to public survey](https://forms.gle/19PKPS17zkL5fTFUA)
* Language implementation: Identified by community as a widely-used language implementation
* Community Addition: Separately identified by the community as important.
* Previously subverted: If software has been previously attacked & it made headlines, it must be critical enough to attack.

Every method for identify critical OSS projects has its strengths and
weaknesses; we believe the combination of analysis combined with human review
is better than trying to do any one of them.
For example, high criticality score tends to emphasize very busy projects;
human review can remove projects that are busy but for whatever reason
are less critical.
Some projects are very important yet not active; by using other measures
(not just the OpenSSF criticality score) we can still identify them.

We have no doubt that other OSS projects will be added to the
critical OSS projects list over time. If you're interested in helping
to do that, please join the Securing Critical Projects WG.

[Here is the list of critical OSS projects and who will be notifying them from the Great MFA Distribution Project](https://docs.google.com/spreadsheets/d/1sO_tJ_B7_2I-TUx23pnBoIRJIqaOm8yBnKAwqs7DwBw/edit#gid=0).
that this list of projects is the same as the list of
  [critical OSS projects identified by the critical projects WG by 2021-12-02](https://docs.google.com/spreadsheets/d/1ONZ4qeMq8xmeCHX03lIgIYE4MEXVfVL6oj05lbuXTDM/edit#gid=0). We're currently using the version as of
2021-12-02, because the Google coupon codes expire on 2021-12-31.
Even if they didn't expire, though, we think it's wiser to quickly get tokens
we have available to critical projects.
The sooner the tokens start getting used by developers, the sooner we
counter some attacks on critical projects.

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
