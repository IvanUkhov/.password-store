# .password-store

The repository contains a home directory of [Pass][pass]. Best enjoyed
responsibly.

## Installation

```bash
brew install gnupg paperkey pass
git clone https://github.com/IvanUkhov/.password-store.git ~/.password-store
gpg --import ~/.password-store/public.txt
gpg --export 13214BE1FEF4E536A7AB7C4F446B464CAC4BB124 > public.key
paperkey --pubring ./public.key --secrets ./private.txt > private.key
gpg --import private.key
```

[pass]: https://www.passwordstore.org/
