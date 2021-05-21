# CLI Cheatsheet

- [Homebrew](#homebrew)
- [Chocolatey](#chocolatey)
- [Git](#git)
- [NVM](#nvm)
- [Docker](#docker)
- [PostgreSQL](#postgresql)
- [Knex](#knex)

## Homebrew

- [CLI reference](https://docs.brew.sh/Manpage)

| Command                                            |
| -------------------------------------------------- |
| `brew search <text\|/text/>`                       |
| `brew install <formula>`                           |
| `brew install --cask <cask>`                       |
| `brew uninstall <formula>`                         |
| `brew list`                                        |
| `brew upgrade <outdated_formula>`                  |
| `` brew update && brew upgrade `brew outdated`  `` |
| `brew analytics off`                               |

## Chocolatey

- [CLI reference](https://docs.chocolatey.org/en-us/choco/commands/)

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
- [Interactive rebase](https://git-scm.com/docs/git-rebase#_interactive_mode)

Create git alias:

```
git config --global alias.pushd "push -u origin HEAD"
git pushd
```

| Zsh Alias     | Command                                                |
| ------------- | ------------------------------------------------------ |
| `gst`         | `git status`                                           |
| `glg`         | `git log --stat`                                       |
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

| Command                                     |
| ------------------------------------------- |
| `nvm use`                                   |
| `nvm use --lts`                             |
| `nvm alias default 14`                      |
| `nvm ls`                                    |
| `nvm ls-remote \| grep -i "<node_version>"` |
| `nvm install <node_version>`                |
| `nvm install --lts`                         |
| `nvm uninstall <node_version>`              |

## Docker

- [docker CLI reference](https://docs.docker.com/engine/reference/commandline/cli/)
- [docker-compose CLI reference](https://docs.docker.com/compose/reference/)

| Command                                          | Description                                                           |
| ------------------------------------------------ | --------------------------------------------------------------------- |
| `docker ps`                                      | list containers                                                       |
| `docker ps -a`                                   | list all containers                                                   |
| `docker ps -aq`                                  | list all container ids                                                |
| `docker images`                                  | list downloaded images                                                |
| `docker cp <container_id>:<src_path> <dst_path>` | copy from container to local machine                                  |
| `docker cp <src_path> <container_id>:<dst_path>` | copy from local machine to container                                  |
| `docker rm`                                      | remove container                                                      |
| `docker rm $(docker ps -aq)`                     | remove all containers                                                 |
| `docker rmi [-f] <image>`                        | remove image                                                          |
| `docker stop <container_id>`                     |                                                                       |
| `docker exec -it <container_id> <command>`       | run CLI command inside the container                                  |
| `docker-compose up -d`                           | builds, (re)creates, starts, and attaches to containers for a service |
| `docker version`                                 |                                                                       |
| `docker-compose version`                         |                                                                       |

## PostgreSQL

- [psql](https://www.postgresql.org/docs/current/app-psql.html)
- [Cheatsheet](https://tomcam.github.io/postgres/)

| Command                                                     | Description                                           |
| ----------------------------------------------------------- | ----------------------------------------------------- |
| `psql -h <hostname> -p <port> -U <username> -d <dbname> -W` | connect to database (-W option means propmt password) |
| `\h`                                                        | help                                                  |
| `\q`                                                        | quit                                                  |
| `\l`                                                        | list databases                                        |
| `\dt`                                                       | display tables                                        |
| `\du`                                                       | display user roles                                    |

## Knex

- [Migrations CLI reference](https://knexjs.org/#Migrations-CLI)
- [Cheatsheet](https://devhints.io/knex)

| Command                            | Description                                      |
| ---------------------------------- | ------------------------------------------------ |
| `knex init`                        | create new knex file                             |
| `knex migrate:make migration_name` | create migration file                            |
| `knex migrate:latest`              | run all migration that has not yet been run      |
| `knex migrate:rollback`            | rollback the last batch of migrations            |
| `knex migrate:rollback --all`      | rollback all the completed migrations            |
| `knex migrate:up`                  | run the next migration that has not yet been run |
| `knex migrate:down`                | undo the last migration that was run             |
| `knex migrate:list`                | list both completed and pending migrations       |
