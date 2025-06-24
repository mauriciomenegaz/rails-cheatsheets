# Setup ubuntu dev environment

## Install node using asdf

https://asdf-vm.com/guide/getting-started.html

## Useful keyboard shortcuts (kde)

Move focus to another screen / desktop:
- Meta + Control + Left / Meta + Control + Right

Move current window to another screen / desktop:
- Meta + Shift + Left / Meta + Shift + Right

## KDE configs

- Settings / Workspace Behaviour / Virtual Desktops
  - desabilitar wrap around
  - animacao: fade desktop, 500ms

- Settings / Shortcuts / Kwin
  - Switch one desktop to the left
  - Switch one desktop to the right


- Settings / Window Management / Task Switcher
  - Thumbnail Grid
  - Trocar a tecla de atalho de alternar entre janelas da mesma aplicacao

## Install additional applications

- KWrite
- Kolourpaint
- Spectacle

## Troubleshooting

### Problem with external monitors

- if external monitors show blank after login
rm -rf ~/.local/share/kscreen/*

/home/mauricio/.rbenv/versions/2.7.4/lib/ruby/gems/2.7.0/gems/rb-inotify-0.10.1/lib/rb-inotify/notifier.rb:69:in `initialize': Too many open files - Failed to initialize inotify: the user limit on the total number of inotify instances has been reached. (Errno::EMFILE)

sudo vi /etc/sysctl.d/60-inotify.conf
fs.inotify.max_user_instances = 256


## Dropbox

instalar normalmente (download do .deb na pagina oficial)

instalar dolphin-plugins (https://askubuntu.com/questions/1382551/how-to-install-and-use-dropbox-in-kde)

habilitar plugin do dropbox no dolphin (https://askubuntu.com/questions/1382551/how-to-install-and-use-dropbox-in-kde)

--

## anki

download binario qt6

--

## k9s

baixar binario linux_amd64.deb

--

## Docker

instalar docker engine utilizando apt
https://docs.docker.com/engine/install/ubuntu/
