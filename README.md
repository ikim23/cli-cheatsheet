# CLI Cheatsheet

- [Homebrew](#homebrew)
- [Chocolatey](#chocolatey)
- [Git](#git)
- [NVM](#nvm)
- [Docker](#docker)
- [PostgreSQL](#postgresql)
- [Knex](#knex)

## Homebrew

- [CLI Commands](https://docs.brew.sh/Manpage)

  | Command                           |
  | --------------------------------- |
  | `brew search <text\|/text/>`      |
  | `brew install <formula>`          |
  | `brew install --cask <cask>`      |
  | `brew uninstall <formula>`        |
  | `brew list`                       |
  | `brew upgrade <outdated_formula>` |
  | `brew analytics off`              |

## Chocolatey

- [CLI Commands](https://docs.chocolatey.org/en-us/choco/commands/)

| Command                                     |
| ------------------------------------------- |
| `choco search <filter>`                     |
| `choco install <pkg> [<pkg2> [<pkgN>]]`     |
| `choco uninstall <pkg\|all> [pkg2 [pkgN]]`  |
| `choco list -lo`                            |
| `choco upgrade all`                         |
| `choco upgrade all --except="<pkg[,pkg2]>"` |

## Git

- [zsh git aliases](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git)
- [interactive rebase](https://git-scm.com/docs/git-rebase#_interactive_mode)

```
git config --global alias.pushd "push -u origin HEAD"
git pushd
```

| Zsh Alias     | Command                                                |
| ------------- | ------------------------------------------------------ |
| `gst`         | `git status`                                           |
| `glo`         | `git log --oneline --decorate`                         |
| `gl`          | `git pull`                                             |
| `gp`          | `git push`                                             |
| `gpf`         | `git push --force-with-lease`                          |
| `gpsup`       | `git push --set-upstream origin $(git_current_branch)` |
| `gco`         | `git checkout`                                         |
| `gcm`         | `git checkout $(git_main_branch)`                      |
| `grhh`        | `git reset --hard`                                     |
| `grb`         | `git rebase`                                           |
| `grba`        | `git rebase --abort`                                   |
| `grbc`        | `git rebase --continue`                                |
| `grbm`        | `git rebase $(git_main_branch)`                        |
| `grbd`        | `git rebase develop`                                   |
| `grbi HEAD~3` | `git rebase -i HEAD~3`                                 |

## NVM

- [Call `nvm use` automatically in a directory with a `.nvmrc` file](https://github.com/nvm-sh/nvm#zsh)

| Command                                     | Description |
| ------------------------------------------- | ----------- |
| `nvm use`                                   |             |
| `nvm use --lts`                             |             |
| `nvm alias default 14`                      |             |
| `nvm ls`                                    |             |
| `nvm ls-remote \| grep -i "<node_version>"` |             |
| `nvm install --lts`                         |             |
| `nvm uninstall <node_version>`              |             |

## Docker

- [docker CLI Commands](https://docs.docker.com/engine/reference/commandline/cli/)
- [docker-compose CLI Commands](https://docs.docker.com/compose/reference/)

| Command                  | Description |
| ------------------------ | ----------- |
| `docker ps`              |             |
| `docker cp`              |             |
| `docker rm`              |             |
| `docker rmi`             |             |
| `docker stop`            |             |
| `docker exec -it bash`   |             |
| `docker version`         |             |
| `docker-compose up -d`   |             |
| `docker-compose version` |             |

## PostgreSQL

## Knex

- [Migrations CLI](https://knexjs.org/#Migrations-CLI)
- [Cheatsheet](https://devhints.io/knex)

| Command                            | Description                                      |
| ---------------------------------- | ------------------------------------------------ |
| `knex init`                        |                                                  |
| `knex migrate:make migration_name` | create migration file                            |
| `knex migrate:latest`              |                                                  |
| `knex migrate:rollback`            | rollback the last batch of migrations            |
| `knex migrate:rollback --all`      | rollback all the completed migrations            |
| `knex migrate:up`                  | run the next migration that has not yet been run |
| `knex migrate:down`                | undo the last migration that was run             |
| `knex migrate:list`                | list both completed and pending migrations       |
