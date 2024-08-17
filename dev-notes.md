# Dev Notes

- Branch `mem-test` runs a series of memory tests on helia-coord to assess memory growth over time. There are series of commits and git tags. This is based on helia-coord v1.5.8 using helia 2.1.0 and libp2p 1.2.1.
  - a6ca77 tag: 01-baseline - A baseline measurement with all major features disabled. Low memory usage.
  - 21f863 tag: 02-pubsub-enabled - Pubsub featured enabled. Low memory usage.
  - 9a9cb1 tag: 03-init-connectioin - Initial peer connections made at startup. Starting to see memory usage.
  - 82c8b8 tag: 04-relay-connect - Relay reconnection enabled in timer controller. Significantly increased memory usage.
  - 59532a tag: 05-peer-connect - Peer reconnection enabled in timer controller. Even more memory usage than 04.

- helia-upgrade: is based on commit 919cb1. This upgrades the helia and libp2p dependencies to the latest version, to see if there are breaking changes and if the memory usage is improved.
