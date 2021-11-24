# The Great MFA Distribution Project

## How to use your key

## Token setup

Both the Titan Key and Yubikey support the FIDO standard. FIDO keys generally do not require any special setup on modern systems. Some of the steps
listed below may require newer versions of utilities or libraries, versions will be specified when appropriate

You can test your key by visiting the [yubico demo site](https://demo.yubico.com/webauthn-technical/registration). It is expected this test will work on any modern operationg system and updated web browser. Even though the test site is hosted by yubico, any FIDO key can be tested.

Assuming your test worked, please continue with the how to use instructions below.

## Platform agnostic

### GitHub

GitHub has instructions for enabling a security key for logging into the website
* [Configuring two-factor authentication using a security
key](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication#configuring-two-factor-authentication-using-a-security-key)

At this time FIDO keys cannot be used to commits on GitHub. Please add an upvote to [this discussion](https://github.com/github/feedback/discussions/7744) to enable this feature. The FIDO key can be used to store your SSH key which can be used to push and pull repositories from GitHub. Instructions for using your FIDO key with SSH are included below.

### GitLab

GitLab has instructions for configuring a security key for logging into the website.
* [WebAuthn
device](https://docs.gitlab.com/ee/user/profile/account/two_factor_authentication.html#webauthn-device)

At this time FIDO keys cannot be used to commits on GitLab. Please add an upvote to [this discussion](https://gitlab.com/gitlab-org/gitlab/-/issues/343879) to enable this feature. The FIDO key can be used to store your SSH key which can be used to push and pull repositories from GitLab. Instructions for using your FIDO key with SSH are included below.

### NPM

NPM does not support security keys at this time. To use MFA you must use an authenticator app.
* [Configuring two-factor
authentication](https://docs.npmjs.com/configuring-two-factor-authentication)

A package can be configured to require MFA when publishing
* [Requiring 2FA for package publishing and settings modification](https://docs.npmjs.com/requiring-2fa-for-package-publishing-and-settings-modification)

When the 2FA option is configured, the updates can only happen interactively.
* [See the --otp option](https://docs.npmjs.com/cli/v8/commands/npm-publish)

### PyPI

PyPI has instructions to configure a security key.
* [How does two factor authentication with a security device (e.g. USB key) work?
How do I set it up on PyPI?](https://pypi.org/help/#utfkey)

Using a security key with PyPI is only needed to login to the website. Packages can still be pushed using a username and passowrd or an API token. The PyPI API token documentation can be found [here](https://pypi.org/help/#apitoken).

### RubyGems

RubyGems does not support security keys. To use MFA you must use an
authenticator app.
* [SETTING UP MULTIFACTOR
AUTHENTICATION](https://guides.rubygems.org/setting-up-multifactor-authentication/)

### SSH

A FIDO key can be configured to work with SSH. This means ssh authentication can only happen with the security plugged into the machine. A very nice writeup of how to use a FIDO key to generate and store SSH keys can be found [here](https://www.stavros.io/posts/u2f-fido2-with-ssh/)

This SSH key can then be used to push and pull from Git repositories as well as logging into remote systems. Git version 2.34 and above supports signing commits with an SSH key, however GitHub and GitLab do not support verifying SSH signatures at this time.
