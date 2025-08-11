# Jogo da Velha com Busca em Largura (BFS)

Este projeto é uma implementação do **Jogo da Velha** onde a jogada da IA (representada pelo 'O') é otimizada utilizando o algoritmo de **Busca em Largura (BFS)**. O jogo permite que um jogador humano jogue contra a IA, com a IA tentando encontrar a melhor jogada possível de maneira eficiente.

## Algoritmo Utilizado: Busca em Largura (BFS)

O algoritmo **Busca em Largura** (Breadth-First Search – BFS) é uma técnica de busca utilizada para explorar todos os possíveis estados de um problema de forma iterativa e em níveis. Em vez de buscar a solução em um único caminho, o BFS explora todas as possibilidades em cada "nível" de profundidade antes de avançar para o próximo nível.

### Como o BFS é aplicado no Jogo da Velha

Neste projeto, o algoritmo BFS foi aplicado para encontrar a melhor jogada para a IA, jogando com o 'O'. A IA, representada pelo 'O', faz a busca pela vitória mais próxima, explorando todas as possibilidades de movimento a partir do estado atual do tabuleiro. 

A cada novo movimento da IA, a BFS expande os estados do jogo e verifica se há uma jogada que leve à vitória em um número mínimo de movimentos. Caso não haja uma vitória imediata, o algoritmo continua explorando outras jogadas possíveis.

### Passos do Algoritmo BFS no Jogo da Velha

1. **Estado inicial**: O estado do tabuleiro é armazenado como uma lista 3x3. Cada célula pode estar vazia (`''`), ocupada por 'X' (jogador humano) ou 'O' (IA).

2. **Fila de estados**: A BFS usa uma fila (implementada com `deque`) para explorar todos os estados possíveis. Cada estado é uma configuração do tabuleiro, junto com o caminho de jogadas que levou até aquele estado.

3. **Exploração de estados**: A BFS começa com o estado atual do tabuleiro. A partir desse estado, o algoritmo tenta todas as jogadas possíveis (colocando um 'O' nas células vazias), criando novos estados filhos.

4. **Verificação de vitória**: Para cada novo estado gerado, o algoritmo verifica se a IA ('O') ganhou. Caso a vitória seja detectada, o caminho que levou a essa vitória é retornado como a melhor jogada.

5. **Evitar ciclos**: Para evitar a repetição de estados e ciclos infinitos, o algoritmo mantém um conjunto de estados já visitados.

6. **Resultado**: Se a IA encontrar um caminho para ganhar, ela faz a jogada correspondente. Caso contrário, ela continua explorando novas jogadas até o final do jogo.

## Como Rodar o Projeto

### Requisitos

- Python 3.x
- Pygame

### Instalação

1. Clone o repositório ou baixe o código:
   ```bash
   git clone https://github.com/seu_usuario/jogo-da-velha-bfs.git
   cd jogo-da-velha-bfs
