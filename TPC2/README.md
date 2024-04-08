# TPC2: Mapa das Ruas de Braga

## 2024-02-05

## Autor
- A100902
- Fábio Daniel Rodrigues Leite

## Resumo
    
Neste trabalho, utilizou-se um dataset em json sobre as cidades de Portugal para criar:
- Uma lista com todas as cidades
- Uma página para cada cidade, apresentando informações sobre a mesma.
- Um serviço em node que faz a conexão entre o input do utilizador no url e a página a apresentar

## Desenvolvimento

**geraIndex.py**: cria a página inicial com a lista das cidades.

**geraPagInd.py**: é responsável por criar as páginas individuais das cidades, com informações sobre elas e as suas ligações

**servidor_ficheiro.js**: é responsável por criar o servidor, que recebendo o input do url devolve a página correspondente.
