# Como configurar/instalar/usar o `remmina` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `remmina` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `remmina` on `Linux Ubuntu`._


## Descrição [2]

### `remmina`

`Remmina` é um cliente de desktop remoto de código aberto que suporta vários protocolos, como `RDP`, `VNC`, `SSH`, `NX`, `XDMCP` e `SPICE`. Ele oferece uma interface intuitiva e fácil de usar para acessar e controlar sistemas remotos de forma segura. Com recursos avançados, como suporte a vários perfis de conexão, compartilhamento de área de trabalho e redimensionamento dinâmico, `Remmina` é uma ferramenta versátil para administradores de sistemas e usuários que precisam acessar máquinas remotas de maneira eficiente e conveniente.


## 1. Como configurar/instalar/usar o `remmina` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `remmina` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```
    

Para instalar o `Remmina` no `Linux Ubuntu` pelo Terminal, você pode seguir os seguintes passos. O `Remmina` é uma aplicação de desktop remoto para sistemas baseados em `Linux` que suporta protocolos como RDP, VNC, SPICE, entre outros. Aqui está como você pode fazer:

1. Primeiro, vamos adicionar o PPA do `Remmina` ao seu sistema para garantir que você tenha a versão mais recente. Execute o seguinte comando: `sudo apt-add-repository ppa:remmina-ppa-team/remmina-next -y`

    Este comando adiciona o PPA (Personal Package Archive) oficial do `Remmina` ao seu sistema, o que permite que você instale a versão mais atualizada.

2. Atualize o índice do pacote do seu sistema para refletir as novas adições do PPA. Para isso, use o comando: `sudo apt update -y`

    Este comando sincroniza a lista de pacotes disponíveis para instalação com os repositórios definidos no sistema, incluindo o PPA do Remmina que você acabou de adicionar.

3. Agora, você está pronto para instalar o `Remmina`. Execute o seguinte comando para iniciar a instalação: `sudo apt install remmina remmina-plugin-rdp remmina-plugin-secret`
    
    Este comando instala o aplicativo `Remmina` juntamente com plugins para suporte a RDP (Remote Desktop Protocol) e para gerenciamento de senhas seguras (plugin secret).

Depois de completar esses passos, o `Remmina` estará instalado no seu sistema Ubuntu e pronto para ser usado. Você pode iniciar o `Remmina` procurando-o no menu de aplicações ou executando remmina no `Terminal Emulator`.

### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `remmina` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean                                                            
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt-add-repository ppa:remmina-ppa-team/remmina-next -y
    sudo apt update
    sudo apt install remmina remmina-plugin-rdp remmina-plugin-secret -y
    ```


## Referências

[1] OPENAI. ***Instalar remmina no ubuntu.*** Disponível em: <https://chat.openai.com/c/586f8f0a-8543-4d9f-9f60-98a2fb51a611> (texto adaptado). Acessado em: 05/04/2023 17:11.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 05/04/2024 17:10.

