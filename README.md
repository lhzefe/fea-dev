# FEA.dev: Python para negócios

Curso de Python para negócios instruido pela FEA.dev da USP (Universidade de São Paulo).

[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org)
[![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)](https://www.anaconda.com/)
[![FEA.dev](material-de-referencia/images/fea-dev-badge.png)](https://github.com/fea-dev-usp)
[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/lhzefe)

## Índice

- [Sobre](#sobre)
- [Introdução](#introdução)
  - [Roteiro](#roteiro)
  - [Requisitos](#requisitos)
  - [Instalações](#instalações)

## Sobre

Esse repositório se propõe a guiar o seu utilizador no aprendizado da linguagem Python e algumas de suas ferramentas, com foco na relação entre **Programação de Computadores e Negócios**.

O cronograma e a metodologia base, aqui apresentados, são de propriedade intelectual da FEA.dev USP e segue fomentado pelo autor desse repositório, o qual agrega guias de instalação de ferramentas, bibliotecas, além de disponibilização de *cheat sheets* e outras referências.

## Introdução

### Roteiro

| Tema  | Bibliografia |
| ------------- | ------------- |
| Introdução ao curso e ao Python | Learning Python, Capítulos 1, 2, 4, 5 e 7 |
| Lógica de programação | Learning Python, Capítulos 12 e 13 |
| Loops e Condicionais | Learning Python, Capítulos 12 e 13 |
| Funções | Learning Python, Capítulos 5, 8 e 16 |
| Introdução a bibliotecas e Numpy | Python for Data Analysis, Capítulo 4 |
| Pandas I - Análise de Dados | Python for Data Analysis, Capítulo 5 |
| Pandas II - Análise de Dados | Python for Data Analysis, Capítulo 5 |
| Visualização de dados | Python for Data Analysis, Capítulo 8 |
| Projeto Final | Toda a bibliografia |

### Requisitos

Para se obter uma boa experiência com esse repositório, indico a seguir o que será necessário:

- [Chocolatey](#chocolatey)
- [Anaconda 3](#anaconda3)
- [Python 3.9.12+](#python)
  - [Numpy](#numpy)
  - [Pandas](#pandas)
- [Visual Studio Code](#vsc)
  - [Extensões](#vsc-ext)
- [Jupyter Notebook](#jupyternb)

### Instalações

O passo-a-passo para instalar o ferramental necessário encontra-se na sequência. Mas vale lembrar que algumas ferramentas são opcionais, porém como são itens que me geram certo conforto para trabalhar, vou coloca-los aqui, afinal, vai que meu conforto pode também ser o seu :).

Importante ressaltar que grande parte dos comandos de terminal podem pedir nível de permissão de administrador, assim, se em algum momento se deparar com um erro de nível de autorização, provavelmente é isso. Sendo assim, instale com administrador.

Se quiser, é possível ir direto no site do [Anaconda](https://www.anaconda.com) e utilizar uma instalação padrão Windows (next, next, next..) vai funcionar... mas eu particularmente acho o Anaconda puro muito pesado, e demora demais para abrir, me lembra a um Eclipse com JBoss (para quem usa ou se lembra). Não me entenda mal, eu tenho ele instalado, se precisar, ele ta ali me esperando. Fora que o core de Python dele já vem recheado de bibliotecas então se eu precisar e alguma coisa tiver acontecido com o meu Visual Studio Code, a "Jibóia" ta ali esperando (rsrs).

De modo geral eu gosto do combo: Visual Studio Code + Python + Extensão do Jupyter Notebook para Visual Studio Code. E se você for que nem eu, mas não quiser ter o Anaconda de segunda opção, eu recomendo instalar o **Chocolatey**, posteriormente os comandos a seguir e é isso. Contudo, acredito ser fortemente interessante que seja lido todo o conteúdo desse README, para que se tenha em mente as variações de instalação, trazendo assim, flexibilidade. E como aqui estamos tratando de Windows, voltamos ao next, next, next, se te fizer maior conforto.

```powershell
choco install vscode python vscode-python vscode-jupyter 
```

Após finalizadas as instalações acima, reinicia a sessão do Powershell é necessário para que as intalações tenham efeito. Existem algumas maneiras de fazer isso... feche e abra o Powershell (rsrs).

Por fim com o Powershell aberto uma vez mais, instale o Pandas que carrega consigo indiretamente, Numpy e diversas outras bibliotecas a serem usadas nos códigos desse repositório.

```powershell
pip install pandas 
```

- Chocolatey <a name="chocolatey"></a> (Opcional)

O [chocolatey](https://chocolatey.org) é um gerenciador de pacotes para Windows. De modo geral, ele lembra muito ao [Homebrew](https://brew.sh) para quem usa MacOS ou linux.

Para instalar o gerenciado de pacotes, acesse o Powershell (Terminal) com o comando: `CTRL + R`, digite **powershell** e aperte Enter.
No terminal copie e cole o comando abaixo e em seguida o execute apertando enter:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
Se tudo correr bem, ao final você receberá uma mensagem dizendo que está tudo okey. Por fim pode digitar: `choco -v` e apertar enter para visualizar a versão do Chocolatey que foi instalada.

Com o Chocolatey instalado, é possível basicamente instalar de uma só vez o Anaconda, Python, Visual Studio Code e Jupyter Notebook, além de diversos outras aplicações ([lista de aplicações](https://community.chocolatey.org/packages))como o próprio Git no qual esse repositório se encontra.

- Anaconda 3 <a name="anaconda3"></a> (Opcional)

Assim, vamos com o comando abaixo instalar o Anaconda 3 Python, Visual Studio Code e Jupyter Notebook:

```powershell
choco install anaconda3
```

- Python <a name="python"></a>

Observe que, caso o Anaconda tenha sido instalado ele por si só já instala o Python e varias bibliotecas para **Ciência de dados** e **Aprendizado de máquina**, como: **Numpy** e **Pandas**.

Todavia, com o comando que segue, vamos instalar o Python:

```powershell
choco install python
```

```powershell
pip install pandas
```

- Visual Studio Code <a name="vsc"></a>

Instalando o Visual Studio Code com as extensões: **Python** e **Jupyter**:

```powershell
choco install vscode vscode-python vscode-jupyter
```

- jupyter Notebook <a name="jupyternb"></a>

O jupyter Notebook foi instalado utilizando pelo Anaconda ou como uma extensão no Visual Studio Code. Para tal, siga um dos passos anteriormente apresentados.

Caso você tenha instalado apenas o Pyhon é possível também instalar apenas o Jupter Notebook clássico pela terminal utilizando o comando **pip**:

```powershell
pip install notebook
```
