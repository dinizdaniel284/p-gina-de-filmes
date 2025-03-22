# página-de-filmes
"Página de filmes com FastAPI e dashboard do Power BI"

# API de Filmes com FastAPI

Este é um projeto de API de filmes criado com **FastAPI** e utilizado para análise de dados de filmes. A API oferece funcionalidades de consulta, inserção e remoção de filmes, além de permitir filtrar por gênero e ano de lançamento.

## Funcionalidades

- **GET /movies**: Retorna uma lista de filmes. Pode ser filtrada por **gênero** ou **ano de lançamento**.
- **POST /movies**: Adiciona um novo filme à base de dados.
- **DELETE /movies/{movie_id}**: Remove um filme pelo seu ID.

## Como Executar

1. Clone este repositório para sua máquina local:
    ```bash
    git clone https://github.com/SEU_USUÁRIO/api-de-filmes.git
    ```

2. Instale as dependências necessárias:
    ```bash
    pip install -r requirements.txt
    ```

3. Execute o aplicativo:
    ```bash
    uvicorn main:app --reload
    ```

4. Acesse a API localmente em `http://127.0.0.1:8000`.

## Como Usar

1. **Filtrar Filmes por Gênero**:
   - Exemplo: `GET /movies?genre=Action`

2. **Filtrar Filmes por Ano**:
   - Exemplo: `GET /movies?year=2010`

3. **Adicionar um Filme**:
   - Exemplo: `POST /movies` com os parâmetros `title`, `year`, `genre`.

4. **Remover um Filme**:
   - Exemplo: `DELETE /movies/{movie_id}`

## Descrição do Código

A API foi desenvolvida usando o framework **FastAPI**, que permite a construção rápida de APIs RESTful. A lógica de cada endpoint é simples e direta:

- **GET /movies**: Retorna todos os filmes ou filtra de acordo com os parâmetros `genre` e `year`, usando **list comprehensions**.
- **POST /movies**: Adiciona um novo filme à lista, gerando automaticamente um ID único para o novo filme.
- **DELETE /movies/{movie_id}**: Remove um filme com base no ID fornecido, utilizando um filtro simples para localizar o filme.

## Tecnologia Usada

- **FastAPI**: Framework para a construção de APIs rápidas.
- **Uvicorn**: Servidor ASGI para rodar a aplicação FastAPI.
- **Python 3.x**

## Licença

Este projeto é licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
