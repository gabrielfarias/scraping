# Projeto de automação de coleta de dados na web (scraping) de indicadores financeiros na UOL Economia

Este projeto consiste em um script Python para automatizar a coleta de dados de indicadores financeiros da página de câmbio da UOL Economia.
Os dados coletados são salvos em um banco de dados PostgreSQL.

Página web de raspagem: "https://economia.uol.com.br/cotacoes/cambio/"

## Instalação

1. Certifique-se de ter o Python instalado. Você pode baixá-lo em [python.org](https://www.python.org/downloads/).

2. Clone este repositório em sua máquina local:
    ```
    git clone https://github.com/gabrielfarias/scraping.git
    ```

3. Navegue até o diretório do projeto:
    ```
    cd scraping
    ```

4. Instale as dependências necessárias utilizando pip:
    ```
    pip install -r requirements.txt
    ```

## Uso

1. Execute o script Python para coletar os dados:
    ```
    python scraping_monetario.py
    ```

## Banco de Dados

Antes de executar o script, certifique-se de ter configurado o banco de dados PostgreSQL. Você pode usar as seguintes instruções SQL para criar o banco de dados e a tabela necessários:

```sql
-- Crie a base de dados
CREATE DATABASE dados_financeiros;

-- Conecte-se ao banco de dados
\c dados_financeiros;

-- Crie a tabela para armazenar os indicadores financeiros
CREATE TABLE indicadores_financeiros (
    id SERIAL PRIMARY KEY,
    nome_indicador VARCHAR(255) NOT NULL,
    valor_indicador VARCHAR(50) NOT NULL,
    data_indicador DATE NOT NULL
);

```

## Nota: Chrome e ChromeDriver

Para executar a automação de navegação web, é necessário ter o Google Chrome e o ChromeDriver instalados em sua máquina. Certifique-se de que eles estejam instalados e configurados corretamente antes de executar o script.

