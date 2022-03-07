# Snippets

## Ambientes Virtuais

### Miniconda

Para gerenciamento de pacotes e de ambientes virtuais do Python, será utilizada a ferramenta [MINICONDA](https://docs.conda.io/en/latest/miniconda.html).

#### Instalação

[Miniconda Installation](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)

É importante marcar a opção de configurar o caminho do python como sendo o padrão, durante a instalação.

Pode ser que haja conflito entre variáveis de ambiente (definição do caminho do python) no sistema operacional. Dessa forma, é interessante verificar as variáveis de ambiente do sistema, e corrigí-las.

Verificando as variáveis de ambiente no Windows:
No prompt de comandos, powershell, ou afins, utilizar o seguinte comando irá retornar uma lista de todas as variáveis de ambiente do Windows.

    set

Para corrigir as variáveis de ambiente envolvidas no Conda/Python, pode-se utilizar o seguinte comando, após instalação do miniconda.

    conda init

### Utilização de Ambientes Virtuais

#### Criando um ambiente virtual

    conda create {env_name}

#### Utilizando o ambiente criado

    conda activate {env_name}

#### Instalando packages no ambiente virutal

    conda install {package_name}

Caso não haja o package disponível através do 'conda install', pode-se utilizar do PIP. Para tal, o PIP deve ser chamado dentro do ambiente virtual (após o conda activate), pois dessa forma, será utilizado o interpretador python do ambiente virtual, e não mais o interpretador global, instalando o package apenas no ambiente ativado.

    python -m pip install {package_name}
    