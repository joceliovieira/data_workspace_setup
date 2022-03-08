# Configuração Global

Aqui estão contidas informações sobre a configuração 'global' das máquinas. Isto é, a nível de sistema operacional. Portanto, deve ser a primeira parte da configuração.

## Descrição

A máquina a ser utilizada será baseada em Linux. Assim, caso o sistema operacional da mesma seja Windows, deverá ser utilizado o WSL2 (Windows Subsystem for Linux). Para detalhes, conferir a [documentação do WSL2](https://docs.microsoft.com/en-us/windows/wsl/about).

Para realizar a instalação de softwares e afins, no sistema utilizado (Linux Ubuntu), será utilizada a ferramenta [Homebrew](https://brew.sh/).

A IDE utilizada será o Visual Studio Code.

Abaixo, é possível verificar a arquitetura das soluções envolvidas.

![arquitetura](/img/arquitetura_global.drawio.svg)

### WSL2

Definição (documentação oficial): _The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a traditional virtual machine or dualboot setup._

#### Instalação

Windows Powershell/CMD como administrador:

    wsl --install -d ubuntu

### Homebrew

Documentação: <https://docs.brew.sh/Manpage>

Definição (documentação oficial): _Homebrew is the easiest and most flexible way to install the UNIX tools Apple/Linux didn’t. It can also install software not packaged for your Linux distribution to your home directory without requiring sudo._

Opera de forma semelhante ao Anaconda, sendo que no âmbito do sistema operacional, e não mais no(s) ambiente(s) Python.

#### Instalação

Após acessar o ambiente WSL, é realizada a instalação do brew através da seguinte linha de comando.

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Após a instalação inicial, deve-se definit o 'PATH' do brew. Para tal, basta seguir os comandos exibidos no terminal, na seção de 'Next Steps'.

#### Utilização

    brew command [--verbose|-v] [options] [formula]

Exemplo

    brew install wget

### Visual Studio Code

#### Instalação

A IDE será instalada na máquina Host, e acessada através do WSL.

[Instalação VS Code](https://code.visualstudio.com/)

#### Acessando via WSL

Para acessar o Visual Studio Code através do Ubuntu, basta seguir para o diretório de trabalho e executar o comando 'code .'

[WSL - Remote](https://code.visualstudio.com/docs/remote/wsl)

Exemplo - Windows Shell

```PowerShell
cd {path}
wsl
code . 
```

Onde _path_ é o caminho do diretório de trabalho.

## Próximos Passos

Instalado o WSL2 e o Brew, pode-se seguir para a configuração/instalação dos ambientes de desenvolvimento Python e Docker.

Para acessar o material deferente a Python clique [aqui](\python.md), e Docker, [aqui](\docker.md).
