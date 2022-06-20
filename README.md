# rs-project-template

rust project template

## QuickStart:

### Requirements:

- cookiecutter

```ruby

# Mac OS X install cookiecutter:
brew install cookiecutter

# Python + pipx:
brew install pipx
pipx ensurepath
pipx install cookiecutter

# Debian/Ubuntu:
sudo apt-get install cookiecutter

```

- go-task:

```ruby

brew install go-task/tap/go-task

```

### Usage:

> create monorepo:

```yml

# cd your-workspace/
# rust monorepo:  git@github.com:better-rs/rs-template.git
new:mono:
    cmds:
        - cookiecutter https://github.com/better-rs/rs-template.git --directory="mono-repo/rs"

```

> test run:

```ruby

task run

# example app:
test cli:run

# example lib:
test core:test

```


## Generate Project Folder Structure:

> monorepo:

```ruby
-> % tree mono/ -L 5 -a
mono/
├── .editorconfig
├── .env.local
├── .github
│   └── workflows
│       ├── rust-clippy.yml
│       └── rust.yml
├── .gitignore
├── .pre-commit-config.yaml
├── .pre-commit-hooks.yaml
├── Cargo.lock
├── Cargo.toml
├── Readme.md
├── Taskfile.yml
├── crates                               // monorepo // rust workspace
│   ├── app                        // your create app
│   │   ├── .gitignore
│   │   ├── Cargo.toml
│   │   ├── Taskfile.yml     // run scripts
│   │   └── src
│   │       └── main.rs
│   ├── cli                        // example app/bin
│   │   ├── .gitignore
│   │   ├── Cargo.toml
│   │   ├── Taskfile.yml     // run scripts
│   │   └── src
│   │       └── bin
│   │           └── main.rs
│   └── core                       // example lib
│       ├── .gitignore
│       ├── Cargo.toml
│       ├── README.md
│       ├── Taskfile.yml           // run scripts
│       └── src
│           └── lib.rs
├── docs
│   └── .gitkeep
├── rustfmt.toml
└── tmp
    └── .gitkeep

12 directories, 27 files


```
