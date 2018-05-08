```sh
brew install gpg                    # cli
brew cask install gpg-suite         # macos pref pane + keychain integration
gpg --key-gen                       # make key

# produces this:

# /Users/cbnz/.gnupg/pubring.kbx
# ------------------------------
# pub   rsa2048 2018-05-08 [SC] [expires: 2020-05-07]
#       E2B0DD890A5926E124F8468A563E9ADC0A394F28
# uid           [ultimate] Carl Bennett <carlbennettnz@gmail.com>
# sub   rsa2048 2018-05-08 [E] [expires: 2020-05-07]

# using the last 8 chars of the id/hash/whatever:

git config --global user.signingkey 0A394F28 # use key with git
git config --global commit.gpgsign true      # or per repo, or use `git commit -S` per commit
```
