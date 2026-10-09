# 🤖 Automação de Cadastro de Produtos com Python

Automação de tarefas repetitivas desenvolvida com **Python, PyAutoGUI e Pandas** para automatizar o cadastro de produtos em um sistema web de treinamento por meio da interface gráfica do navegador.

O projeto utiliza uma base de dados CSV com 293 produtos e automatiza o preenchimento dos campos de um formulário web, aplicando conceitos de manipulação de dados e automação de processos.

## 📌 Sobre o projeto

O cadastro manual de centenas de produtos pode ser uma tarefa repetitiva e demorada. Este projeto explora como a automação com Python pode simplificar esse processo, utilizando dados estruturados para preencher formulários de maneira sequencial.

A interação com o sistema ocorre por meio do controle do mouse e do teclado, sem utilizar uma API para realizar os cadastros.

## ✨ Funcionalidades

* Abertura do Google Chrome.
* Acesso à página de login do sistema.
* Preenchimento automatizado dos campos de autenticação.
* Leitura de dados de um arquivo CSV com Pandas.
* Processamento sequencial dos registros.
* Preenchimento automatizado dos campos do formulário.
* Envio dos cadastros por meio da interface gráfica.
* Controle de pausas entre as etapas da automação.

## 🛠️ Tecnologias utilizadas

| Tecnologia    | Aplicação                             |
| ------------- | ------------------------------------- |
| Python        | Linguagem principal                   |
| PyAutoGUI     | Controle do mouse e teclado           |
| Pandas        | Leitura e processamento dos dados     |
| CSV           | Armazenamento dos produtos            |
| Time          | Controle de pausas durante a execução |
| Google Chrome | Navegador utilizado na automação      |

## 🔄 Fluxo de execução

```text
       produtos.csv
            │
            ▼
    Leitura com Pandas
            │
            ▼
    Iteração dos produtos
            │
            ▼
    Preenchimento do formulário
           PyAutoGUI
            │
            ▼
       Envio do cadastro
            │
            ▼
      Próximo produto
```

## 📂 Estrutura do projeto

```text
automacao-cadastro-produtos/
├── pegar_posicao.py
├── produtos.csv
├── requirements.txt
├── .gitignore
└── README.md
```

| Arquivo            | Descrição                                                         |
| ------------------ | ----------------------------------------------------------------- |
| `pegar_posicao.py` | Script principal responsável pela automação da interface gráfica. |
| `produtos.csv`     | Base de dados com os produtos utilizados na automação.            |
| `requirements.txt` | Lista de dependências Python necessárias para executar o projeto. |
| `.gitignore`       | Define arquivos e diretórios que não devem ser versionados.       |

## 📊 Estrutura dos dados

O arquivo `produtos.csv` contém 293 registros, organizados nas seguintes colunas:

| Campo            | Descrição                       |
| ---------------- | ------------------------------- |
| `codigo`         | Código identificador do produto |
| `marca`          | Marca do produto                |
| `tipo`           | Tipo do produto                 |
| `categoria`      | Categoria do produto            |
| `preco_unitario` | Preço unitário                  |
| `custo`          | Custo do produto                |
| `obs`            | Observações adicionais          |

Os valores são lidos pelo script e utilizados para preencher os campos correspondentes no formulário web.

## 🚀 Como executar o projeto

### Pré-requisitos

* Python 3 instalado.
* Google Chrome instalado.
* Sistema operacional Windows.
* Acesso ao sistema web de treinamento utilizado pelo projeto.

### 1. Clone o repositório

```bash
git clone https://github.com/Mateus-DB/automacao-cadastro-produtos.git
```

Entre na pasta do projeto:

```bash
cd automacao-cadastro-produtos
```

> Se o nome do repositório for diferente, ajuste a URL e o nome da pasta conforme necessário.

### 2. Crie um ambiente virtual

```bash
python -m venv .venv
```

Ative o ambiente virtual no PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

Ou, no Prompt de Comando (CMD):

```bat
.venv\Scripts\activate.bat
```

### 3. Instale as dependências

```bash
python -m pip install -r requirements.txt
```

O arquivo `requirements.txt` deve conter:

```text
pandas
PyAutoGUI
```

### 4. Prepare o ambiente

Antes de iniciar, verifique as coordenadas dos elementos utilizados pelo PyAutoGUI. A posição dos campos deve corresponder à interface do sistema.

Mantenha o Google Chrome visível e em primeiro plano durante a execução. Como a automação controla o mouse e o teclado, evite interagir com outras janelas enquanto o processo estiver ativo.

### 5. Execute a automação

```bash
python pegar_posicao.py
```

O script executará as etapas definidas no código para interagir com o sistema web e processar os produtos.

## ⚠️ Limitações técnicas

A automação baseada em interface gráfica apresenta algumas limitações:

* **Dependência de coordenadas:** alterações na resolução, escala do Windows, zoom ou layout podem afetar os cliques.
* **Dependência da janela ativa:** se outra aplicação receber o foco, a digitação poderá ocorrer no local incorreto.
* **Sincronização:** pausas fixas podem não ser suficientes quando a página demora a carregar.
* **Validação dos resultados:** o envio do formulário não garante, por si só, que o cadastro foi salvo corretamente.

Essas limitações devem ser consideradas durante a execução e em possíveis evoluções do projeto.

## 🔧 Possíveis melhorias

* Implementar tratamento de exceções.
* Validar os dados antes de preencher os formulários.
* Adicionar logs de execução.
* Confirmar o resultado de cada cadastro.
* Gerar um relatório de sucessos e falhas.
* Melhorar a identificação e ativação da janela do navegador.
* Substituir coordenadas fixas por seletores DOM utilizando Playwright ou Selenium, caso a abordagem seja compatível com o objetivo do projeto.
* Adicionar testes automatizados para as rotinas de processamento de dados.

## 🎓 Contexto do projeto

Projeto de aprendizado desenvolvido no contexto dos estudos de Python pela **Hashtag Treinamentos**, com foco na prática de automação de tarefas repetitivas, manipulação de dados com Pandas e controle de interfaces gráficas com PyAutoGUI.

O objetivo é aplicar os conceitos estudados em um cenário prático de automação de cadastro de produtos.

## 🎯 Conhecimentos demonstrados

* Desenvolvimento de scripts em Python.
* Automação de interfaces gráficas.
* Conceitos de RPA (*Robotic Process Automation*).
* Manipulação de dados com Pandas.
* Leitura e processamento de arquivos CSV.
* Iteração sobre registros estruturados.
* Automação de tarefas administrativas repetitivas.
* Documentação e organização de projetos.

## 👨‍💻 Autor

**Mateus Demartino Bastos**

Desenvolvedor com foco em desenvolvimento web, aplicações Full Stack e automações.

* GitHub: [@Mateus-DB](https://github.com/Mateus-DB)
* LinkedIn: [Mateus Demartino](https://linkedin.com/in/mateus-demartino)

---

*Projeto de aprendizado desenvolvido para praticar Python e automação de processos.*
