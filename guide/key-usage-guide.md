# The Great MFA Distribution Project

## How to use your key

## Token setup

FIDO keys generally do not require any special setup on modern systems. Some of the steps
listed below may require newer versions of utilities or libraries, versions will be
specified when appropriate

You can test your key by visiting the [yubico demo
site](https://demo.yubico.com/webauthn-technical/registration).
It is expected this test will work on any updated web browser.

Assuming your test worked, please continue with the how to use instructions

## Platform agnostic

### GitHub

GitHub has instructions for enabling a security key to login
* [Configuring two-factor authentication using a security
key](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication#configuring-two-factor-authentication-using-a-security-key)

### GitLab

GitLab has instructions for configuring a security key to login
* [WebAuthn
device](https://docs.gitlab.com/ee/user/profile/account/two_factor_authentication.html#webauthn-device)

### NPM

NPM does not support security keys. To use MFA you must use an authenticator
app.
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

### RubyGems

RubyGems does not support security keys. To use MFA you must use an
authenticator app.
* [SETTING UP MULTIFACTOR
AUTHENTICATION](https://guides.rubygems.org/setting-up-multifactor-authentication/)

### SSH

A FIDO key can be configured to work with SSH. This means ssh authentication can only happen with the security plugged into the machine.
* [How to use FIDO2 USB authenticators with SSH](https://www.stavros.io/posts/u2f-fido2-with-ssh/)
