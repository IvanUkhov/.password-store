# .password-store

The repository contains a home directory of [Pass][pass]. Best enjoyed
responsibly.

## Usage

Install the requirements and clone the repository:

```bash
brew install gnupg paperkey pass
git clone https://github.com/IvanUkhov/.password-store.git ~/.password-store
```

In order to import the private key, obtain `private.txt` and run:

```bash
gpg --import public.txt
gpg --export $(cat .gpg-id) > public.key
paperkey --pubring public.key --secrets private.txt > private.key
gpg --import private.key
```

In order to export the private key, run:

```bash
gpg --export-secret-key $(cat .gpg-id) | paperkey > private.txt
```

[pass]: https://www.passwordstore.org/
