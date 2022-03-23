# Oque vamos desenvolver
Nesse projeto vamos desenvolver um jogo de adivinhar palavras inspirado no  [Wordle](https://www.nytimes.com/games/wordle/index.html)

# Como o jogo funciona?
## Objetivo
O objetivo é adivinhar uma palavra aleatória de 5 letras, após uma tentativa você recebe dicas sobre as letras

- Amarelo: A letra existe mas está no lugar incorreto
- Verde A letra existe e está no lugar correto

Com essas dicas o jogador precisa deduzir a palavra correta em menos de 6 tentativas

## Inspirações
Caso você queira entender na pratica como o jogo funciona dê uma olhadinha nos links abaixo

[Wordle](https://www.nytimes.com/games/wordle/index.html) (Versão original em inglês)
[Letreco](https://www.gabtoschi.com/letreco/) (Versão em português)
[term.ooo](https://term.ooo/) (Versão em português com opções de jogar com 1, 2 ou 4 palavras)


# Requisitos
Para poder ser participar da votação, o seu código **OBRIGATORIAMENTE** precisa cumprir atender os pontos abaixo

- [ ] Deve ser possível jogar uma palavra aleatória
- [ ] Deve mostrar as dicas corretas
- [ ] Deve exibir a palavra correta após o Player acertar
- [ ] Deve conter os testes para as funcionalidades
	- [ ] As dicas são mostradas corretamente
	- [ ] Ao final do jogo é exibido uma 
- [ ] Fazer o deploy
- [ ] Preencher o formulário de participação

# Sugestão de como desenvolver
As sugestões abaixo são apenas um guia para poder facilitar o desenvolvimento, mas sinta-se livre para fazer da forma que preferir desde que os requisitos estejam sendo atendidos

## 1 - Criar um Input de texto para o usuário enviar a palavra

### Oque é esperado

- Deve conter um input
- A Palavra deve ser armazenada

## 2 - Construa uma tabela com 6 linhas () e 5 colunas (Quantidade de letras)

### O que é esperado

- Ter um quadro com 6 linhas`<tr>` (Quantidade de tentativas)
- Ter um quadro com 5 colunas `<td>` (Quantidade de letras)

## 3 - Criar um botão para enviar o Input

### Oque é esperado

- O botão está desabilitado quando a palavra contem menos ou mais de 5 letras
- Ao clicar a palavra ser mostrada na linha da tabela (Uma letra em cada célula)

## 3 - Criar um botão para limpar o Input

### Oque é esperado
- O input é limpo após clicar no botão

## 4 - Pegar uma palavra randomica do arquivo (no data) para ser a palavra chave
### O que é esperado

- Quando a aplicação carregue, uma palavra randomica
- Guardar a palavra selecionada em um gerenciador de Estado (Redux ou Context)

## 5 - Implementar a logica de verificação
### Oque é esperado
- Armazenar oque o usuario digitou
- Verificar a posição das letras (Amarelo = letra existente no lugar errado e verde = lugar certo)
- Mostra um aviso caso a palavra não exista no banco de palavras

## 6 - Implementa a logica de verificação da palavra chave
### Oque é esperado
 - Se o usuario acertar
	- Verica-se é redirecionado para a tela de feedback
- Se o usuario errar
	- Ir para a proxima linha
- Se o usuario errar e não tiver mais tentativas
	- Redirecionar para a tela de feedback

## 7 - Feedbacks

- Deve mostrar uma mensagem de acordo com o numero de tentativas

### Exemplo:
| Tentativas            | Resultado     |
|-----------------------|---------------|
| Menos de 3 tentativas | Excelente     |
| > 3 e > 5 tentativas  | Muito bom     |
| 6 tentativas          | Foi por pouco |
| Não tiver acertado    | Você perdeu   |
