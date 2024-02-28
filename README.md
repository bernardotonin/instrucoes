# Passo a passo

## Criação do projeto python
1. Crie uma pasta no local desejado e copie o endereço absoluto da pasta ([Imagem](https://i.imgur.com/kiTqtKl.png))
2. `cd <endereço que você copiou>`
3. `python3 -m venv env` -> Cria o ambiente virtual do Python
4. `call .\env\Scripts\activate.bat` -> Ativa o ambiente virtual
5. Pronto, agora basta instalar os pacotes desejados com `pip install <nome-do-pacote>`

> Nota:
> Lembrando que em ambientes proxy, é necessário usar a flag --proxy, exemplo: 
> `pip install --proxy http://usuario:senha@<proxy-server>:<port> <nome-do-pacote>`<br>
> O pip também permite instalação de varios pacotes, separando por espaços:
> `pip install <nome-do-pacote> <nome-do-pacote> ...` 

## Criação do Git
1. `cd <pasta desejada>`
2. `git init` -> Inicia o repositório local Git
3. `git add .` -> Adiciona todos os arquivos untracked
4. `git commit -m "<mensagem-desejada>"` -> Commita alterações<br>

	> Nota:
	> [Conventional commits](https://www.conventionalcommits.org/en/v1.0.0/#summary) -> Padrão de mercado das mensagens de commit 
6. `git branch -M main` -> Muda o nome da branch, que por padrão é master, para main.
7. `git remote add origin https://github.com/<seu usuário>/<repositorio>.git` -> Adiciona um repositório remoto no repositório local ([Onde conseguir esse link](https://i.imgur.com/9fRWz6t.png))
8. `git push -u origin main` -> Envia as alterações para o repositório remoto<br />
	> Autenticação:
	> Git Credential Manager: Se o GCM estivar instalado, ao executar o push, uma janela vai abrir pedindo para se autenticar pelo navegador.
	Comandos: ao executar o push, o Git vai solicitar seu usuário do GitHub e a senha, que nesse caso será o token, que pode ser criado [nesse link](https://github.com/settings/tokens). (Obs: criar o token [clássico](https://i.imgur.com/1c2HsNc.png))

## Links úteis
[Pypi](https://pypi.org/)<br />
[PyAutoGui](https://pyautogui.readthedocs.io/en/latest/)<br />
[MouseInfo](https://mouseinfo.readthedocs.io/en/latest/)<br />
> Passo a passo do MouseInfo:
> 1 - Abra a prompt de comando
> 2 - `pip install mouseinfo` -> instala o pacote do Mouse Info
> 3 - `python3` -> abre o console do python3
> 4 - `import mouseinfo` -> importa o modulo do Mouse Info
> 5 - `mouseinfo.MouseInfoWindow()` -> chama a função que abre a janela do Mouse Info
>
> Por que não preciso criar um ambiente virtual para instalar esse pacote?
> -> Por padrão, a instalação já cria um ambiente virtual "global", que abriga esses pacotes, independente do diretório em que a prompt de comando está.

[Documentação do Python](https://docs.python.org/3/)
