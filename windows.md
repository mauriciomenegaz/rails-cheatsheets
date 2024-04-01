# Step by Step Dev Environment Setup (windows version)

## 1) wsl (wsl --install)
 -> https://learn.microsoft.com/en-us/windows/wsl/setup/environment

## 2) visual studio code

## 3) zsh / ohmyzsh

- https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH
- https://github.com/ohmyzsh/ohmyzsh

## 4) rbenv (usando rbenv-installer(?))

- instalar dependências (https://github.com/rbenv/ruby-build/wiki) - suggested build environment
- rbenv-installer: https://github.com/rbenv/rbenv-installer#rbenv-installer (using curl)

6) postgresql
- ver tutorial "windows wsl development environment"
  -> https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-database
  -> https://www.atlassian.com/data/admin/how-to-set-the-default-user-password-in-postgresql

pra conectar do pgadmin, setar essa linha no postgresql.conf:

`listen_addresses = '*'`

criar usuario
```
CREATE ROLE mauricio;
ALTER ROLE mauricio WITH login;
ALTER ROLE mauricio WITH superuser;
```


7) node - install from node source

   https://github.com/nodesource/distributions

8) yarn - usando o npm

```sudo npm install --global yarn```

9) redis - usando o  repositorio deles


   https://redis.io/docs/install/install-redis/install-redis-on-windows/

10) chrome no wsl

plano a: chrome for testing instalado automaticamente com o selenium:

 a.1 instalar dependencias:
 (ver https://github.com/puppeteer/puppeteer/blob/main/docs/troubleshooting.md)

sudo apt install ca-certificates fonts-liberation libasound2 libatk-bridge2.0-0 \
  libatk1.0-0 libc6 libcairo2 libcups2 \
  libdbus-1-3 libexpat1 libfontconfig1 libgbm1 \
  libgcc1 libglib2.0-0 libgtk-3-0 libnspr4 \
  libnss3 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 \
  libx11-6 libx11-xcb1 libxcb1 libxcomposite1 \
  libxcursor1 libxdamage1 libxext6 libxfixes3 \
  libxi6 libxrandr2 libxrender1 libxss1\
  libxtst6 lsb-release wget xdg-utils

  a.2 rodar o script de teste do selenium que tambem instala chrome e chromedriver

  gem install selenium-webdriver
  ruby test_chrome.rb (arquivo esta nesta pasta)

  a.3 se nao funcionar, disparar o chrome na mao e ver qual erro ta dando



plano b: chrome full
  -> baixar o instalador do chrome para ubuntu
  -> sudo dkpg -i
  -> sudo apt-get -f install
  -> google-chrome --headless --disable-gpu --screenshot https://www.chromestatus.com/

11) git - configuracoes uteis:

```
  git config --global pager.branch false
  git config --global pager.log false
  git config --global user.name "Mauricio Menegaz"
  git config --global user.email "mauricio.menegaz@gmail.com"
```

12) vs code - extensoes

[Guia de configuracao do VS Code](vscode.md)

13) ngrok
  - instalar via apt

14) sublime merge
    - instalar dentro do wsl (interface grafica usa wslg)
    - https://www.sublimemerge.com/docs/linux_repositories
    - comando: smerge

15) windows terminal

nomes dos atalhos que tem que configurar:
- Guia Anterior: Control + Page Up
- Próxima Guia: Control + Page Down
