# homebrew-briefcred

The Homebrew tap for [briefcred](https://github.com/vkend/briefcred), a local,
biometric-gated credential broker for AI agents and developer tooling.

```sh
brew install vkend/briefcred/briefcred
briefcred install --trust-ca      # start the daemon and trust its local CA
briefcred profile bootstrap       # write a first profile
```

After `brew upgrade briefcred`, move the running daemon onto the new binary
without dropping a session:

```sh
briefcred daemon upgrade
```

Don't use `brew services` for briefcred; `briefcred install` manages the
LaunchAgent.

macOS only. The binaries are universal (Apple silicon and Intel), signed with
a Developer ID and notarised by Apple.

`Formula/briefcred.rb` is copied from the `briefcred.rb` asset of each
[release](https://github.com/vkend/briefcred/releases); the source of truth is
[`release/Formula/briefcred.rb`](https://github.com/vkend/briefcred/blob/main/release/Formula/briefcred.rb)
in the main repository.
