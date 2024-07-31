# Git

## Git Cheat Sheets

- https://education.github.com/git-cheat-sheet-education.pdf
- https://training.github.com/downloads/pt_BR/github-git-cheat-sheet/

## Git Flow

- **Instalação do Git Flow:** https://github.com/petervanderdoes/gitflow-avh/wiki/Installation

## Git Flow Cheat Sheets

- https://gist.github.com/matdcooper/e8c617fb5136d95c11a4f4eeab0ab085
- https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

## Comandos Git Flow mais utilizados

- *Inicializando o Git Flow*

```git flow init```

- *Conferir em qual branch se está trabalhando*

```git branch```

- *Iniciar uma nova feature*

```git flow feature start <nome>```

- *Finalizar uma feature (merge na branch develop)*

```git flow feature finish <nome>```

- *Iniciar uma nova release*

```git flow release start <tag>```

- *Finalizar uma nova release (merge na branch main e novo merge na develop se houve alterações)*

```git flow release finish <tag>```

- *Iniciar uma correção/bug*

```git flow hotfix start <nome>```

- *Finalizar uma correção/bug*

```git flow hotfix finish <nome>```

## Assinatura de commit com GPG

- *Verificar a existência de chaves*

```gpg --list-secret-key --keyid-form LONG```

- *Gerar uma chave(RSA)*

```gpg --full-generate-key```

- *Exportar chave pública para configurar no SSH e GPG Keys do GitHub*

```gpg --armor --export <id_da_chave>```

- *Configurar a chave localmente no git para assinar os commits*

```git config --global user.signing <id_da_chave>```

- *Configurar a variável de ambiente para assinatura*

```vim ~/.bash_profile``` e adicionar ao arquivo a variável ```export GPG_TTY=$(tty)```

- *Assinatura dos commits*

```git config commit.gpgsign true```

- *Assinatura global dos commits*

```git config --global commit.gpgsign true```

- *Assinatura das tags*

```git config tag.gpgSign true```

- *Assinatura global das tags*

```git config --global tag.gpgSign true```

- *Verificar assinatura do commit*

```git log --show-signature -1```

- *Adicionar outro email a chave*

```gpg --edit-key <id_da_chave>```
```add uuid``` e cadastra o email
```uid <numero do id>```
```trust```
```save```

## Ferramentas para Auxiliar em Conventional Commits

- **Extensão VSCode:** https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits

- **Commitlint:** https://commitlint.js.org/guides/local-setup.html

- **Commitsar:** https://commitsar.aevea.ee

- **Commitizen:** https://github.com/commitizen/cz-cli