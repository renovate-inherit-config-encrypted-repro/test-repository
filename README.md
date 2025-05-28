# 36214

In this example repository renovate is run via a github action, with the config provided in the renovate-config.js file. The config has a privatekey set, and inheritConfig enabled.
In the [org inherited config companion repository]((https://github.com/renovate-inherit-config-encrypted-repro/renovate-config)) a host rule is configured, with an encrypted token.

## Current behavior

Renovate picks up the host rule from the inherited config, but does not decrypt the token, and instead "complains" that no authentication is set for the host.

## Expected behavior

Renovate should decrypt the token from the inherited config and use it for authentication.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/36214