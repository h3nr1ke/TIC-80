[![Build Status](https://travis-ci.org/nesbox/TIC-80.svg?branch=master)](https://travis-ci.org/nesbox/TIC-80)
[![Build status](https://ci.appveyor.com/api/projects/status/1pflw77cjd8mqggb/branch/master?svg=true)](https://ci.appveyor.com/project/nesbox/tic-80)

![TIC-80](https://tic.computer/img/logo64.png)
**TIC-80 TINY COMPUTER** - [https://tic.computer/](https://tic.computer/)

# Sobre
TIC-80 é um fantasy computer **GRATUITO** e **OPEN SOURCE** para criar, jogar e compartilhar pequenos jogos.

Com TIC-80 você recebe ferramentas integradas para o desenvolvimento: código, sprites, mapas, editores de som e um terminal de linha de comando, o que é suficiente para criar um mini jogo retrô.

Os jogos são empacotados em um arquivo de cartucho (cartridge files), os quais podem ser distribuídos facilmente. TIC-80 funciona em todas nas mais populares plataformas. Isso significa que seu cartucho pode ser jogado em qualquer dispositivo.

Para desenvolver um jogo no estilo retrô, todo o processo de criação e execução existem sob uma série de limitações técnicas: display de 240x136 pixel, paleta de 16 cores, 256 sprites coloridos de 8x8 pixel, 4 canais de som, etc.

![TIC-80](https://user-images.githubusercontent.com/1101448/29687467-3ddc432e-8925-11e7-8156-5cec3700cc04.gif)

### Funcionalidades
- Suporte a múltiplas linguagens de programação: [Lua](https://www.lua.org),
  [Moonscript](https://moonscript.org),
  [Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript),
  [Wren](http://wren.io/), and [Fennel](https://fennel-lang.org).
- Os jogos podem ter suporte a mouse e teclado
- Os jogos podem ter até 4 controles como entrada (com até 8 botões, cada)
- Editores integrados: para codificar, sprites, mapas dos mundos, efeitos sonoros e música
- Um banco de memória adicional: carregar assets diferentes do seu cartucho enquanto o jogo está sendo executado

# Downloads dos Binários
Você pode baixar uma versão compilada para a os maiores sistemas operacionais diretamente na nossa [página de releases](https://github.com/nesbox/TIC-80/releases).

# Versão pro
Para ajudar no desenvolvimento do TIC-80, existe uma [Versão PRO](https://nesbox.itch.io/tic).
Esta versão possui algumas funcionalidades adicionais e os binários podem ser baixados exclusivamente em [nossa página do Itch.io](https://nesbox.itch.io/tic).

Para os usuários que não podem gastar o dinheiro, nós tornamos simples o processo de compilar a Versão Pro a partir do código fonte.

### Funcionalidades da versão Pro

- Salvar/Carregar cartuchos em formato de texto, e criar o jogo em qualquer editor que você desejar, muito útil para controlar a versão utilizando respositórios, como o GitHub.
- Ainda mais bancos de memória: ao invés de ter apenas 1 banco de memória, você tem 8.
- Exporte seu jogo sem os editores, e então publique-os nas lojas de aplicativos (WIP).

# Comunidade
Você pode jogar e compartilhar jogos, ferramentas e músicas em [tic.computer](https://tic.computer/play).

A comunidade também discute diversos assuntos no [Chat do Discord](https://discord.gg/DkD73dP).

# Contribuindo
Você pode controbuir enviando um bug ou requisitando uma nova funcionalidade
 em nossa [página de requisções/bugs](https://github.com/nesbox/tic.computer/issues).
Tenha em mente que você deve seguir o [Código de Conduta](https://github.com/nesbox/TIC-80/blob/master/CODE_OF_CONDUCT.md) sempre que se envolver em discussões do projeto.

Você também pode contribuir revisando e melhorando o conteúdo de nossa [wiki](https://github.com/nesbox/tic.computer/wiki).
A [wiki](https://github.com/nesbox/tic.computer/wiki) aramazena a documentação do TIC-80, exemplos de código e tutoriais de desenvolvimento de jogos.

# Instruções para compilação

## Windows
### com Visual Studio 2017
- instalar `Visual Studio 2017`
- instalar `git`
- execute os comandos a seguir no `cmd`
```
git clone --recursive https://github.com/nesbox/TIC-80 && cd TIC-80/build
cmake -G "Visual Studio 15 2017 Win64" ..
```
- abra `TIC-80.sln` e compile
- aproveite :)

### com MinGW
- instalar `mingw-w64` (http://mingw-w64.org) e adicione o caminho `.../mingw/bin` na *variavel de ambiente PATH*
- instalar `git`
- instalar `cmake` (https://cmake.org)
- execute os comandos a seguir no `terminal`
```
git clone --recursive https://github.com/nesbox/TIC-80 && cd TIC-80/build
cmake -G "MinGW Makefiles" ..
mingw32-make -j4
```

## Linux 
### Ubuntu 14.04
execute os comandos a seguir no terminal
```
sudo apt-get install git cmake libgtk-3-dev libgles1-mesa-dev libglu-dev -y
git clone --recursive https://github.com/nesbox/TIC-80 && cd TIC-80/build
cmake ..
make -j4
```

para instalar a última versão do CMake:
```
wget "https://cmake.org/files/v3.12/cmake-3.12.0-Linux-x86_64.sh"
sudo sh cmake-3.12.0-Linux-x86_64.sh --skip-license --prefix=/usr
```

### Ubuntu 18.04

execute os comandos a seguir no terminal
```
sudo apt-get install git cmake libgtk-3-dev libglvnd-dev libglu1-mesa-dev freeglut3-dev -y
git clone --recursive https://github.com/nesbox/TIC-80 && cd TIC-80/build
cmake ..
make -j4
```

## Mac
instale `Command Line Tools for Xcode` e o gerenciador de pacotes `brew`

execute os comandos a seguir no terminal
```
brew install git cmake
git clone --recursive https://github.com/nesbox/TIC-80 && cd TIC-80/build
cmake ..
make -j4
```

## iOS / tvOS
Você encontra versões para iOS/tvOS aqui 
- 0.60.3: https://github.com/brunophilipe/TIC-80
- 0.45.0: https://github.com/CliffsDover/TIC-80
