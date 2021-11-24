# Q & A

Here is a non-exhaustive list of questions and answers around the project

## Q: Why is the OpenSSF doing this?
A: The security of open source supply chains and infrastructure has grown in importance in recent years.  The OSSF feels projects such as the [Great MFA Distribution](https://github.com/ossf/great-mfa-project)
along with other tools and techniques help improve the security and assurance of the integrity of open source software.

## Q: How do I get an MFA token?
A: The Great MFA Distribution project has identified a list of critical OSS projects we will engage with first.  
Details about the project and how to get a token can be found at the project’s [repository](https://github.com/ossf/great-mfa-project). 

## Q: How do I install and setup an MFA token?
A: Depending on which token you’ve received, there are instructions and links in the project’s [repository](https://github.com/ossf/great-mfa-project#how-do-i-use-an-mfa-token). Don't forget to setup a safe recovery mechanism in case of a lost/broken/misplaced/stolen token.

## Q: How do I log in using an MFA token?
A: Depending on which token you’ve received, there are instructions and links in the project’s [repository](https://github.com/ossf/great-mfa-project#how-do-i-use-an-mfa-token).

## Q: How do I sign software code with an MFA token?
A: Depending on which token you’ve received, there are instructions and links in the project’s [repository](https://github.com/ossf/great-mfa-project#how-do-i-use-an-mfa-token).

## Q: Can I get more than one token for my project?
A: Yes!

## Q: I got my token, but i can’t get it to work.  What can I do?
A: Make sure to follow the instructions carefully and you did not miss any steps. If you are still stuck then we would advise to create a support ticket to get more help on getting it working.

## Q: I set my MFA token up and started using it, but it has subsequently been lost/broken/misplaced/stolen.  What should I do?
A: Most of the code repository platforms offer recovery methods to gain access to the account when you are dealing with a lost/broken/misplaced/stolen token.
For example the most common default fail safe mechanism is the secrets one use codes that you autimatically 

## Q: I set my MFA token up and started using it, but it has subsequently been lost/broken/misplaced/stolen.  What should I do?
A: Most of the code repository platforms offer recovery methods to gain access to the account when you are dealing with a lost/broken/misplaced/stolen token.
For example the most common default fail safe mechanism is the secrets one time use codes that are automatically generated when you enrolled your hardware token. Using this mechanism it’s utterly important to store these secret one time use codes in a safe matter. You can achieve this by printing them out and store them in a physical vault or use a digital secure password storage.

Also when you don’t like this approach there is also per platform other options. For example in [Github](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication-recovery-methods#downloading-your-two-factor-authentication-recovery-codes) you can create a fail safe mechanism that uses your Phone number and per SMS you can still gain access. 
Other platforms like [GitLab](https://about.gitlab.com/blog/2018/08/09/keeping-your-account-safe/) offer a backup email address or using your SSH keys that are connected to the account you can generate new secrets one time use codes.

## Q: Now i have this token I'm not hackable anymore, right?
A: This will increase the level of security and protection for your project immensly but 

## Q: Now i have this token I'm not hackable anymore, right?
A: This will increase the level of security and protection for your project immensely but use your common sense. Do not leave your token unguarded in public or not trusted spaces as there are known [side-channel attacks](https://www.zdnet.com/article/new-side-channel-attack-can-recover-encryption-keys-from-google-titan-security-keys/) for hardware tokens. 
