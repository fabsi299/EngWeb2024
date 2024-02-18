# TPC1: Mapa das Ruas de Braga


## Autor
- A100902
- Fábio Daniel Rodrigues Leite

## Resumo
    
Neste trabalho, utilizou-se material fornecido pelo docente; ficheiro XML com a informação de 60 ruas de Braga; fotos atuais (associadas a uma determinada vista); e fotos dos espaços desenhados no séc. XVIII das mesmas ruas, para produzir um website onde se pode consultar e navegar nesta estrutura.
    
O site apresenta uma página principal com a linha de ruas ordenada alfabeticamente. 
    
Clicando numa das ruas acede-se à página individual da rua onde se pode consultar toda a informação. Nesta página há também um link para regressar à página principal. 

## Desenvolvimento

### index.py

O ficheiro index.py é responsável pela criaçao da página de index. Esta página apresenta um lista de todas as ruas ordenadas por ordem alfabética, acompanhada de um header e um footer simples.

Para a criação da lista, foi formado um dicionário que associava, a cada número de rua, o seu nome, através da iteração dos ficheiros .xml.

### page.py

O ficheiro page.py é responsável pela criaçao das diversas páginas, tornando-o mais complexo.Tal como no index, estas páginas vão apresentar um header e um footer.

Primeiramente foi feita uma itereção sobre os ficheiros .xml de forma a obter o número e nome de cada rua, permitindo a criação do ficheiro HTML de cada  rua.

Seguidamente, para cada ficheiro .xml, faz-se uma  procura pela descrição da rua e por informação sobre a listas de casas, adicionando todo este conteúdo ao ficheiro HTML.

Relativamente às imagens, é feita uma procura nos ficheiros xml pelos caminhos para as imagens correspondentes. Devido à diferença da extensão do dataset (no .xml está em maiúsculas e no dataset em minúscula ou o contrário, exemplo da rua 53), é feita uma modificação da lista de caminhos para as imagens antigas obtidas de forma a que todos os elementos tenham a extensão em minúsculas. Desta forma, é feita a procura pela extensão em minúsculas e, se não for encontrada, procura-se em maiúsculas, tendo a garantia que uma destas será encontrada.

Para as imagens novas, o processo é mais simples, passando apenas pelo uso de uma expressão regular para procurar todas as imagens correspondentes à rua, através do seu número.

Por fim, juntamos todos os elementos no ficheiro HTML.
