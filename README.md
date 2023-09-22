# Dessafio Fullcycle Configurando 

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
gpg --armor --export DCBA2F30A00DB201 
``` 
## Adicionando no GITHUB

 - Alcance o profile do github / settings / gpgkeys / adicionar
 - grava sua chave GPG publica 


