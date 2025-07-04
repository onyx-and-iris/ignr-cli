![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![macOS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)

# ignr

Simple no-frills .gitignore generator backed by the Github API.

![Selection Prompt](./img/selectionprompt.png)

## Install

```console
go install github.com/onyx-and-iris/ignr@latest
```

## Configuration

*flags*

-   --token/-t: GitHub authentication token
    -   note, this tool can be used **without** authenticating but rate limiting will be stricter.
-   --height/-H: Height of the selection prompt (default 10)
-   --filter/-f: Type of filter to apply to the list of templates (default startswith)
    -   may be one of (startswith, contains)
-   --start-search/-s: Start the prompt in search mode (default false)

*environment variables*

```bash
#!/usr/bin/env bash

export IGNR_TOKEN=<API Token>
export IGNR_HEIGHT=10
export IGNR_FILTER=startswith
export IGNR_START_SEARCH=false
```

## Commands

### New

Trigger the selection prompt.

```console
ignr new
```

Search mode can be activated by pressing `/`:

![Prompt Filter](./img/promptfilter.png)

## Special Thanks

-   [spf13](https://github.com/spf13) for the [cobra](https://github.com/spf13/cobra) and [viper](https://github.com/spf13/viper) packages.
-   [Manifold](https://github.com/manifoldco) for the [promptui](https://github.com/manifoldco/promptui) package.
