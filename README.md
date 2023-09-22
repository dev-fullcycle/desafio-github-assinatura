# Desafio Fullcycle Configurando 

## Assinaturas de commits
instalar uma chave GPG pessoal em seu computador 

```bash
# comandos no seu terminal
# verifica as chaves
gpg --list-secret-key --keyid-form LONG
```

```bash
# gera uma chave nova 
gpg --full-generate-key   

```
 - por padrão utilize RSA/4096
 - seu nome
 - email
 - senha para gerar a chave 
```

Agora com a a chave gerada export a chave publica para adiciona-la ao GITHUB  

```bash
gpg --armor --export DCBA2F30A00xxxx 
``` 
## Adicionando no GITHUB

 - Alcance o profile do github / settings / gpgkeys / adicionar
 - grava sua chave GPG publica 

Configura o seu git local na sua maquina 

```bash
git config --global user.signingkey DCBA2F30A00xxxx
```

Inclua no profile da sua maquina esse export
```bash
export GPG_TTY=$(tty)
```
atualizando status do chave GPG
git log --show-signature -1

## adicionando um novo e-mail dentro da sua chave publica 

```bash
gpg --edit-key DCBA2F30A00xxxx

# comnados dentro do gpg
# > adduid - adiciona novo email 
# > preencha os campos de acordo com a 1 vez
# > trust - confie na chave nova 
# > save - finaliza a edicao 
``` 