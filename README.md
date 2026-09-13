# Blackbook

Text social network for the Black Internet Alliance. Part of [BIA](https://github.com/acndintllc/bia-platform) — the
Black Internet Alliance.

Blackbook is a text-first social feed, federated with the other BIA social application over
ActivityPub. Members sign in with one BIA account across every app.

## Status

Repository initialised. The Misskey fork has not landed yet.

## Built on Misskey

Blackbook derives from [Misskey](https://github.com/misskey-dev/misskey), a
federated microblogging platform, licensed **AGPL-3.0**. That license
carries forward: this repository is AGPL-3.0, and so is anything derived
from it.

Bringing the base in:

```bash
git remote add upstream https://github.com/misskey-dev/misskey
git fetch upstream develop
git merge upstream/develop --allow-unrelated-histories
```

## Why this is a separate repository

BIA core — authentication, billing, identity and storage — lives in
[bia-platform](https://github.com/acndintllc/bia-platform) and is not
AGPL-derived. Keeping the Misskey fork in its own repository keeps each
codebase's licensing self-contained.

**Blackbook talks to BIA core over HTTP and never imports it.** Arm's-length
API calls between separate programs do not create a derivative work;
import statements are a far harder argument to make. Keep that boundary.

## License

AGPL-3.0. See [LICENSE](LICENSE).

Copyright (c) 2026 ACND INT. LLC.
Portions copyright the Misskey contributors, from which this work derives.

Run a modified version as a network service and you must offer your users
its complete source. That is the deal Misskey offered, and it carries
forward unchanged.
