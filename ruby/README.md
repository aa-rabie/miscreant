# miscreant.rb [![Latest Version][gem-shield]][gem-link] [![Build Status][build-image]][build-link] [![Yard Docs][docs-image]][docs-link] [![MIT licensed][license-image]][license-link] [![Gitter Chat][gitter-image]][gitter-link]

[gem-shield]: https://badge.fury.io/rb/miscreant.svg
[gem-link]: https://rubygems.org/gems/miscreant
[build-image]: https://secure.travis-ci.org/miscreant/miscreant.svg?branch=master
[build-link]: https://travis-ci.org/miscreant/miscreant
[docs-image]: https://img.shields.io/badge/yard-docs-blue.svg
[docs-link]: http://www.rubydoc.info/gems/miscreant/0.3.0
[license-image]: https://img.shields.io/badge/license-MIT-blue.svg
[license-link]: https://github.com/miscreant/miscreant/blob/master/LICENSE.txt
[gitter-image]: https://badges.gitter.im/badge.svg
[gitter-link]: https://gitter.im/miscreant/Lobby

> The best crypto you've never heard of, brought to you by [Phil Rogaway]

[Phil Rogaway]: https://en.wikipedia.org/wiki/Phillip_Rogaway

Ruby implementation of **Miscreant**: Advanced symmetric encryption library
which provides the [AES-SIV] ([RFC 5297]), [AES-PMAC-SIV], and [STREAM]
constructions. These algorithms are easy-to-use (or rather, hard-to-misuse)
and support encryption of individual messages or message streams.

[AES-SIV]: https://github.com/miscreant/miscreant/wiki/AES-SIV
[RFC 5297]: https://tools.ietf.org/html/rfc5297
[AES-PMAC-SIV]: https://github.com/miscreant/miscreant/wiki/AES-PMAC-SIV
[STREAM]: https://github.com/miscreant/miscreant/wiki/STREAM

**AES-SIV** provides [nonce-reuse misuse-resistance] (NRMR): accidentally
reusing a nonce with this construction is not a security catastrophe,
unlike it is with more popular AES encryption modes like [AES-GCM].
With **AES-SIV**, the worst outcome of reusing a nonce is an attacker
can see you've sent the same plaintext twice, as opposed to almost all other
AES modes where it can facilitate [chosen ciphertext attacks] and/or
full plaintext recovery.

For more information, see the [toplevel README.md].

[nonce-reuse misuse-resistance]: https://github.com/miscreant/miscreant/wiki/Nonce-Reuse-Misuse-Resistance
[AES-GCM]: https://en.wikipedia.org/wiki/Galois/Counter_Mode
[chosen ciphertext attacks]: https://en.wikipedia.org/wiki/Chosen-ciphertext_attack
[toplevel README.md]: https://github.com/miscreant/miscreant/blob/master/README.md

## Help and Discussion

Have questions? Want to suggest a feature or change?

* [Gitter]: web-based chat about miscreant projects including **miscreant.rb**
* [Google Group]: join via web or email ([miscreant-crypto+subscribe@googlegroups.com])

[Gitter]: https://gitter.im/miscreant/Lobby
[Google Group]: https://groups.google.com/forum/#!forum/miscreant-crypto
[miscreant-crypto+subscribe@googlegroups.com]: mailto:miscreant-crypto+subscribe@googlegroups.com?subject=subscribe

## Security Notice

Though this library is written by cryptographic professionals, it has not
undergone a thorough security audit, and cryptographic professionals are still
humans that make mistakes. Use this library at your own risk.

## Requirements

This library is tested against the following MRI versions:

- 2.2
- 2.3
- 2.4
- 2.5

Other Ruby versions may work, but are not officially supported.

## Installation

Add this line to your application's Gemfile:

```ruby
gem "miscreant"
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install miscreant

## Documentation

[Please see the Miscreant Wiki](https://github.com/miscreant/miscreant/wiki/Ruby-Documentation)
for API documentation.

[Yard documentation][docs-link] is also available.

## Code of Conduct

We abide by the [Contributor Covenant][cc] and ask that you do as well.

For more information, please see [CODE_OF_CONDUCT.md].

[cc]: https://contributor-covenant.org
[CODE_OF_CONDUCT.md]: https://github.com/miscreant/miscreant/blob/master/CODE_OF_CONDUCT.md

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/miscreant/miscreant

## Copyright

Copyright (c) 2017-2018 [The Miscreant Developers][AUTHORS].
See [LICENSE.txt] for further details.

[AUTHORS]: https://github.com/miscreant/miscreant/blob/master/AUTHORS.md
[LICENSE.txt]: https://github.com/miscreant/miscreant/blob/master/LICENSE.txt
