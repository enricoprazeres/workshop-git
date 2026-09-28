# Guia auxiliar para o Workshop

## Gerar Chave SSH

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

```
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/utilizador/.ssh/id_ed25519): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/utilizador/.ssh/id_ed25519
Your public key has been saved in /home/utilizador/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:AbCdEf123456GHiJkLmNoPqRsTuVwXyZ0123456789a esprazj.bjj@gmail.com
The key's randomart image is:
+--[ED25519 256]--+

|    . . .        |
|     + o .       |
|    = * .        |
|   = = B .       |
|  . o * S        |
| . . = o .       |
|  . o + .        |
|   . o=          |
|    .==+         |
+----[SHA256]-----+

```

## Clonar o repositório localmente
O primeiro passo é trazer o projeto para a tua máquina.

Corre o seguinte comando no teu terminal:

> Atenção: Antes disso, repara que ao escreveres o comando no terminal, vai aparecer a seguinte mensagem:

```
The authenticity of host 'github.com (140.82.121.4)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJ7nicBMli2WP+Vca7HbbILz2oHCnFI.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```

A isso, deves escrever somente "yes".

Agora que já sabes disso, corre o comando: 

```
git clone git@github.com:enricoprazeres/workshop-git-26-27.git
```

Entra na pasta que acabaste de dar clone:

```
cd workshop-git-26-27/
```

## Criar uma nova branch
Num projeto partilhado, nunca deves trabalhar diretamente na `main` branch. Cria uma branch nova para a tua contribuição:

```
git checkout -b <nome-da-branch>
```

Para o nome da branch, nós do CeSIUM costumamos seguir um padrão:

```
<iniciais>/<feature>
```

Exemplo:

```
ep/add-readme
```

## Fazer as alterações na Branch e o Commit
Faz as modificações que quiseres (por exemplo, adicionar o teu nome a um ficheiro). Depois de guardares o ficheiro, diz ao git para preparar essas alterações:

```
git add .
```

Agora, guarda as alterações com uma mensagem sobre o que fizeste: 

```
git commit -m "feat: add my name to the participants list"
```

## Enviar as alterações
As tuas alterações ainda só existem no teu computador. Vamos enviá-las para o repositório no GitHub:

git push origin <iniciais>/<feature>

## Abrir o Pull Request no GitHub

1. Vai à página deste repositório no GitHub
2. Vais ver uma aviso a verde a dizer que a tua branch teve pushes recentes, com um botão "Compare & Pull Request". Clica nele.
3. Garante que a branch base (para onde queres enviar) é a `main` e a de origem (a tua) é a branch que acabaste de criar.
4. Dá um título ao teu PR, escreve uma breve descrição se necessário, e clica em "Create pull request"

Parabéns! Acabaste de submeter o primeiro PR.

- O comando `git push` deu erro? Verifica se escreveste o nome da branch corretamente.
- Algum problema com os commits? Levanta a mão, os mentores do workshop estão cá para ajudar! Chama algum deles.
