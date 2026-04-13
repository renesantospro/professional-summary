# Professional Summary - Renê Santos

Este repositório contém o código-fonte e a infraestrutura do site profissional/portfólio de **Renê Santos - Engenheiro de Dados**. O projeto utiliza uma abordagem de Documentação como Código (*Docs-as-Code*) para gerar um site estático rápido, elegante e versionado.

## Estrutura do Projeto e Artefatos

*   **`docs/`**: Contém o conteúdo das páginas do site em formato Markdown. O manifesto principal (`index.md`) reflete o perfil "Engenharia de Dados com Mente Industrial", detalhando stacks tecnológicas, mindset e contatos.
*   **`mkdocs.yml`**: Arquivo de configuração do Framework [MkDocs](https://www.mkdocs.org/). Ele orquestra o site definindo o tema ([Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)), cores, fontes, extensões e a estrutura de navegação.
*   **`.github/workflows/deploy_workflow.yml`**: Pipeline de CI/CD configurado no via GitHub Actions. Sempre que um código é mesclado na branch `main`, a Action constrói a aplicação MkDocs e realiza o upload dos artefatos do build automaticamente para um **Bucket no Amazon S3**.
*   **`requirements.txt`**: Dependências Python utilizadas para construir o site estático no ambiente de integração contínua (CI).
*   **`resume_experimental.txt`**: Artefato em texto estruturado contendo o currículo consolidado e detalhado.

## Tecnologias e Infraestrutura

*   **Front-end Estático:** MkDocs & Material for MkDocs.
*   **CI/CD:** GitHub Actions.
*   **Hospedagem Cloud:** AWS S3 (Amazon Simple Storage Service) para entrega global via Web de forma altamente escalável e segura.

## Desenvolvimento Local (Como executar)

Para testar e pré-visualizar o site na sua máquina local antes de gerar um `commit`:

1.  Certifique-se de ter o Python 3.10+ instalado.
2.  (Opcional, mas recomendado) Crie e ative um ambiente virtual:
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # No Windows: .venv\Scripts\activate
    ```
3.  Instale os pacotes com o `pip`:
    ```bash
    pip install -r requirements.txt
    ```
4.  Suba o servidor embutido de desenvolvimento:
    ```bash
    mkdocs serve
    ```
5.  Acesse **[http://localhost:8000](http://localhost:8000)** em seu navegador. O site possui *Hot-Reload* automático à medida que você altera os arquivos dentro da pasta `docs/`.