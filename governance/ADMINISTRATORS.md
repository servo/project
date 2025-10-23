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
