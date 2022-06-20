# rs-project-template

rust project template

## QuickStart:

```yml

    # cd your-workspace/
    # rust monorepo:  git@github.com:better-rs/rs-template.git
    new:mono:
        cmds:
            - cookiecutter https://github.com/better-rs/rs-template.git --directory="mono-repo/rs"

    # rust lib:
    new:lib:
        cmds:
            - cookiecutter https://github.com/better-rs/rs-template.git --directory="library-repo/rs"

    # rust cli app:
    new:cli:
        cmds:
            - cookiecutter https://github.com/better-rs/rs-template.git --directory="app-repo/cli"

    # rust web server app:
    new:app:
        cmds:
            - cookiecutter https://github.com/better-rs/rs-template.git --directory="app-repo/server"

```
