# Security Rationale

Here we identify potential attacks/issues and our countermeasures.

## Project worries tokens may be subverted by the OpenSSF or someone who subverts the OpenSSF

The OpenSSF does not ever possess any tokens distributed by
this project, nor does the OpenSSF send any tokens.
The only thing the OpenSSF distributes are coupon codes / validation codes that
can be eventually used on the Google Store / GitHub Shop (respectively)
to turn an item that costs money into something that is free.

Recipients can verify (through the URL's domain) that they are on
the proper sites, and they use HTTPS which counters interception
during the no-cost "purchase". GitHub token recipients will have to
send the validation code to a GitHub site to turn it into a coupon code,
but again, all of these protections apply.

The recipients do have to trust that Google Store and GitHub Shop
won't send subverted devices to them or share their personal information
(such as addresses) elsewhere. Both do require personal information,
However, this would be true for any shop, and these are reputable shops.

## Project worries personal information may be shared with OpenSSF or someone who subverts the OpenSSF

The OpenSSF never receives the actual names or addresses
of the recipients. The OpenSSF is asking projects to report back
summary metrics. GitHub will learn the GitHub accounts of those who
use the validation codes, but GitHub will only share totals
back to the OpenSSF.
We think it's reasonable that someone who is willing to create an
account on GitHub and use GitHub to manage their code is also willing
to trust GitHub.

## Codes get mis-shared and tokens end up being used by others

This isn't desired, but it isn't a big deal if it only happens in a few cases.
If the tokens end up getting used, that means *someone* is
being protected by the tokens, and is likely going to encourage others to
use such tokens.
Our goal is to quickly get tokens out to critical projects so they can be used.
A perfect system that ensures this never happens, but waits another year,
potentially reduces the protection of everyone else.
We believe that getting tokens quickly into people's hands, at the cost
of a few tokens perhaps being used by others, is a trade-off worth making.

Our main concern is someone stealing most or all of the tokens.
Only a few coupon codes / validation codes will be given to each
project, so no one project will be able to do this.
Only a few trusted code senders will be allowed to have
access to the larger set of codes.
In addition, the value of these tokens is typically much less if you
can't verify their pedigree (as they would be if all codes were stolen).
Thus, we believe mass theft is something we've reasonably countered
and is relatively unlikely.

## Tokens get intercepted and subverted en route

Google and GitHub will use usual delivery methods, so this is the same
risk as for anything delivered over mail.
We will tell people to send the tokens to an address they trust.

## Recipients won't use the tokens, or won't use them correctly

We are developing guidance to help users use the tokens correctly.
