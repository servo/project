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
 
To send token to CI admin use 1password: <https://support.1password.com/share-items> or share password protected zip (password and zip should be send over differnet platforms for additional security).
