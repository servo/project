# Servo Administrators

- [Emilio Cobos Álvarez (@emilio)](https://github.com/emilio)
- [Josh Matthews (@jdm)](https://github.com/jdm)
- [Manish Goregaokar (@Manishearth)](https://github.com/Manishearth)
- [Martin Robinson (@mrobinson)](https://github.com/mrobinson)
- [Samson (@sagudev)](https://github.com/sagudev)

> [!NOTE]
> Check the [`README.md` file](README.md) for more information about the Servo project governance model.

## Administrators work

Administrators have access to [1password team](https://servo-team.1password.com) and [GitHub organistation setting](https://github.com/organizations/servo/settings/profile).

### Issuing tokens for the CI monitor service (self-hosted runners)

To get a `GITHUB_TOKEN` for the monitor service in production:

- [Create](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) a [fine-grained personal access token](https://github.com/settings/personal-access-tokens/new)
    - Token name: `servo <name> monitor` where `name` is name of ci monitor
    - Resource owner: **servo**
    - Expiration: **90 days**
    - Repository access: **Public Repositories (read-only)**
    - Organization permissions > **Self-hosted runners** > Access: **Read and write**

To get a GITHUB_TOKEN for testing the monitor service:

- [Create](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) a [fine-grained personal access token](https://github.com/settings/personal-access-tokens/new)
    - Token name: `servo ci monitor test`
    - Resource owner: your GitHub account
    - Expiration: **7 days**
    - Repository access > **Only select repositories** > your clone of servo/servo
    - Repository permissions > **Administration** > Access: **Read and write** (unfortunately there is no separate permission for repository self-hosted runners)
 
> [!NOTE]
> Ideally tokens are always rotated before they expire.
> However, it can sometimes happen that tokens expire, which causes the runners to go offline.

> [!TIP]
> In cases where we have redundant runners, it is recommended to create at least 2 different tokens, with differing expiration times (ideally 30+ days apart).
> This prevents all runners from going offline if a token expires, and gives us leeway to rotate tokens in an orderly manner, since only a portion of runners will go down at a time if a token was not rotated in time.
 
To send token to CI admin use 1password: <https://support.1password.com/share-items> or share password protected zip (password and zip should be sent over different platforms for additional security).

All active tokens are listed here: <https://github.com/organizations/servo/settings/personal-access-tokens/active>

## Dependabot tokens

The servo repository has a [workflow](https://github.com/servo/servo/blob/main/.github/workflows/auto-merge-updates.yml) for automatically merging and approving pull requests from dependabot.
This workflow requires that the token be generated from the @servo-bot user account.
Credentials for the @servo-bot account is available on 1password.
Note that the token needs to be created under the 'Secrets and Variables > Dependabot' page instead of the usual 'Secrets and Variables > Actions' page.

## Automated sync tokens

We currently have two automated sync setups:

- [servo -> servo-book](https://github.com/servo/servo/blob/main/.github/workflows/book-export.yml): Used to sync content from `servo/servo` to `servo/servo-book`
- [mozjs security bumo](https://github.com/servo/mozjs/blob/main/.github/workflows/security-bump.yml): Used to sync ESR security updates from upstream Spidermonkey releases to `mozjs`

For each of these setups two tokens are required (to limit the permissions granted to the tokens, specifically avoiding giving `Contents: Write` permissions on the upstream repository).
The tokens should be generated from the @servo-bot user account - credentials are available on 1password.

The tokens should be added to the upstream repository as secrets (e.g. `servo/servo`).
Note: When regenerating tokens after expiration, it should be sufficient to hit the regenerate button, and update the secret value.
Before regenerating, keep in mind that this immediately revokes the current token, so check for running actions before regenerating.
For tokens that are used frequently it might makes sense to generate a new token, and revoke the old token only after updating the secret value.

### Token 1 (push branch to servo-bot fork)

The first token is used to push changes to the repository fork under the `servo-bot` user account.
Login as the servo-bot user and create a new personal access token, by navigating to <https://github.com/settings/personal-access-tokens/new>.
Token name: `servo-bot-<repo>-push`.
Resource owner: **servo-bot**
Expiration: Custom (1 year)
Repository access: `Only select repositories` and select `servo-bot/<repo>`.
Permissions: `Contents`: `Read and write`. For `mozjs security bump`, additionally `Workflows: Read and write` is required.

Repository secret names: 

- The push token for `servo -> servo-book` should be added as a secret to `servo/servo` with the name `BOOK_SYNC_TOKEN`.
- The push token for `mozjs security bump` should be added as a secret to `mozjs` with the name `SERVO_BOT`.

### Token 2 (Open PR against the upstream repository)

The second token is required to open a PR against the upstream repository.
Again, login as the servo-bot user and create a new personal access token, by navigating to <https://github.com/settings/personal-access-tokens/new>.
Token name: `servo-<repo>-pull-request`.
Resource owner: **servo** (NOT `servo-bot`)
Expiration: Custom (1 year)
Repository access: `Only select repositories` and select `servo/<repo>`.
Permissions: `Pull requests`: `Read and write`

Since the token is created with `servo` as the resource owner, the token request must be manually approved by a servo admin afterwards.
This approval is not required when regenerating an existing token.

Repository secret names:

- The PR token for `servo -> servo-book` should be added as a secret to `servo/servo` with the name `BOOK_SYNC_CREATE_PR_TOKEN`.
- The PR token for `mozjs security bump` should be added as a secret to `mozjs` with the name `PR_TOKEN`.
