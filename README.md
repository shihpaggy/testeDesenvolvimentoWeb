# Teste de Desenvolvimento Web - BlastOff
> Data de início: 14/06/2022 11:35

**Nome do participante:**
    Shih Chi Shih
    
**Email:**
    paggy.shih@gmail.com

**Linkedin:**
    https://www.linkedin.com/in/shih-chi-shih/

**Github:**
    https://github.com/shihpaggy
    
## Questão 1
> Construa os elementos básicos para formar uma página HTML. Ela não precisa ter nenhum conteúdo.

A estrutura essencial para a construção da página em HTML é mostrado abaixo. 

```
<!DOCTYPE html>
<html>
    <head>
        <title>Título da página</title>
    </head>

    <body>
        Conteúdo HTML aqui
    </body>
</html>
```

Afim de uma melhor preparação do conteúdo, algumas definições metas são indispensáveis no *head* do documento, como a biblioteca de caracteres e *viewport* da tela em que a página será carregada, além da indicação sobre a língua em que o conteúdo mostrado apresentada. Vale ressaltar que a falta destes não afetam na construção do *site*, mas o torna melhor definido e, assim, evitando erros de apresentação.

```
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Nome da pagina</title>
    </head>

    <body>
        Conteúdo HTML aqui
    </body>
</html>
```

## Questão 2
>  Em um determinado projeto os cabeçalhos devem estar previamente definidos com fonte Arial, devem estar em negrito e em caixa alta. Como você faria para esses parâmetros serem implementados neste projeto? 

Existem diversas maneiras de preparar um cabeçalho com fonte Arial, em negrito e caixa alta. Uma delas seria utilizando CSS. Utilizando seletores de elemento, deve incluir seguintes atribuições na folha de estilo:

```
h1, h2, h3, h4, h5, h6{
    font-family: Arial;
    font-weight: bold;
    text-transform: uppercase;
}
```

O trecho de codigo anterior seleciona as tags de título do HTML e os atribui. Contudo, pensando num projeto onde nem todo conteúdo dessas tags precisam de transformações, o método da criação de classe também seria válido.

```
.containerCabecalho{
    font-family: Arial;
    font-weight: bold;
    text-transform: uppercase;
}
```

Assim, para os cabeçalhos que precisam estar definidos com fonte Arial, em negrito e em caixa alta, basta adicionar a classe `containerCabecalho` e terá o mesmo resultado.

## Questão 3
> Construa utilizando HTML e JavaScript um link que ao ser clicado, abre um alerta do navegador.

Para a adição de *pop out* da alerta, uma pequena função em JavaScript deve ser executada. 

```
function exibeAlerta(){
    alert("Alerta!");
}
```

Neste exercício, é necessário uma âncora no corpo do HTML para a inclusão do *Link* que, por agora, é vazio. Para esta interação, é necessário o atributo `onclick` na âncora. Segue abaixo o código.

```
<a href="#" onclick="exibeAlerta()">Link aqui</a>
```

## Questão 4
> Descreva em CSS a seguinte regra: todos os itens de uma lista devem estar orientados na vertical.

Por padrão, os itens de uma lista é exibida verticalmente. Para garantir a sua visualização, pode-se incluir a lista em um *flex container* e utilizar o seguinte trecho CSS:

```
.containerLista{
    display: flex;
    flex-direction: column;
}
```

Para utilizar o código, basta adinionar a classe `containerLista` para o container mãe dos itens da lista.

## Questão 5
>  Descreva em CSS a seguinte regra: somente o último item de uma lista não deve ter uma linha na sua base.

Para começar, deve-se adicionar as linhas base para todos os itens da lista.

```
li{
    text-decoration: underline;
}
```

Como indica no enunciado, deve-se retirar a decoração apenas do ultimo elemento filho da lista. Assim, vale ressaltar a importância das pseudo-classes, o que permite a seleção das tags de uma forma mais clara e eficiente. Para o exercício, `:last-child` deve ser utilizado conforme o código abaixo.

```
li:last-child{
    text-decoration: none;
}
```

## Questão 6
> Um arquivo externo chamado styles.css precisa ser carregado na página HTML. Escreva o código para fazer tal carregamento.

Arquivos externos de CSS devem ser incluidos no *head* do HTML com a seguinte configuração:

```
<link rel="stylesheet" href="styles.css">
```

## Questão 7
> Um dos critérios de um determinado projeto é que todos os links devem ficar sublinhados quando o usuário passar o mouse por cima deles. Escreva o código para garantir essa regra. 

Os efeitos descritos acima podem ser adicionados com o seletor `:hover`. Segue a aplicação abaixo.

```
a:hover {
    text-decoration: underline;
}
```

## Questão 8
> Escreva um comando JavaScript onde o texto Hello World! seja exibido no console do navegador através de uma variável.

Para o início da atividade, é nescessário definir a frase a ser exibida como uma variável.

```
let mensagem = 'Hello World!';
```

Assim, é possível imprimir no console da página a `mensagem` desejada.

```
console.log(mensagem);
```

## Questão 9
> Usando o mesmo código da questão anterior, substitua o texto que será exibido no console do navegador para Hello Toodoo! O novo valor deve sobrescrever o valor original.

Para a exibição da nova frase, deve-se atribuir um novo valor para a variável `mensagem` criada no exercício anterior. Assim, o código sobrescreve a mensagem armazenada na memória.

```
mensagem = 'Hello Toodoo!';
```

## Questão 10
> Desenvolva via JavaScript a seguinte estrutura de código levando em consideração as seguintes regras:
>> a) Uma variável deve ter o nome de sorvete de chocolate;
>> b) Se o seu valor for igual a chocolate, deve ser exibido no alerta do navegador a mensagem: Amo sorvete de chocolate;
>> c) Se o seu valor for outro, deve exibir a mensagem: Prefiro outros sabores.

Para resolução deste exercício, deve-se criar a variável `sorveteDeChocolate`.

```
let sorveteDeChocolate;
```

Assim, é possível montar a estrutura de verificação com base nas regras fornecidas:

```
if(sorveteDeChocolate == 'chocolate'){
    alert('Amo sorvete de chocolate');
}else{
    alert('Prefiro outros sabores');
}
```

## Questão 11
> Na função JavaScript a seguir, responda quais serão os resultados respectivos:

 ```
function multiplicacao (num1,num2) {
    let resultado = num1 * num2;
    return resultado;
}

multiplica(4, 7);
multiplica(5, 6);
multiplica(3, 3);
```

Quando executado o código acima, não será obtido nenhum valor. O nome da função apresentada é `multiplicacao`, contudo, quando chama a função cujo nome `multiplica` dará um erro de referência. Para corrigir o erro é simples, basta trocar o nome da função para multiplica e executar novamente o código e dará resultados de: 28, 30 e 9.

```
function multiplica (num1,num2) {
   let resultado = num1 * num2;
    console.log(resultado);
    return resultado;
    }

multiplica(4, 7);
multiplica(5, 6);
multiplica(3, 3);
```

## Questão 11 (2)
> Em CSS existe uma maneira de sobrescrever um estilo, quando não há outra maneira, além dessa, de se fazer isso. Qual das propriedades a seguir é utilizada para isso? 

(a) force
(b) strong
**(c) !important**
(d) nenhuma das alternativas

Nas hierarquias CSS, para casos de ambiguidade em que duas regras são iguais ou competem, o que usa `!important` prevalece.

## Questão 12
> Analisando a estrutura CSS a seguir, qual cor prevalecerá no elemento HTML?

```
li.list-item {
    color: red;
}
.list-item {
    color: blue
}
#list .list-item {
    color: green
}
ul li {
    color: black;
}
```
**(a) red**
(b) blue
(c) green
(d) black

Em casos de ambiguidades no CSS, deve considerar a especificidade dos seletores. Neste caso, o seletor `li.list-item` é o mais específico, portanto, o elemento aparece na cor vermelha.

## Questão 13
> Levando em consideração a semântica de código, escreva o HTML de uma tabela que possui as seguintes características:
>> a) Deve possuir 3 colunas (Nome, Idade, Gênero);
>> b) Deve possuir 2 linhas (com dados fictícios);
>> c) E uma última linha com todas as suas colunas mescladas.

```
<table border = "1">
    <thead>
        <tr>
            <th>Nome</th>
            <th>Idade</th>
            <th>Gênero</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Lucas</td>
            <td>24 anos</td>
            <td>Masculino</td>
        </tr>
        <tr>
            <td>Gustavo</td>
            <td>26 anos</td>
            <td>Mascullino</td>
        </tr>
    </tbody>
    <tfoot>    
        <tr>
            <td colspan="3"></td>
        </tr>
    </tfoot>
</table>
```

## Questão 14
> Utilizando grid system, não sendo necessário a responsividade, elabore uma página web que siga o layout indicado.

```
.layout{
    background: #2895e7;
    display: grid;
    grid-gap: 10px;
    grid-template-columns: 20% auto 30%;
    grid-template-rows: auto auto auto;
    text-align: center;
}
.containerHeader{
    background: #d3eafc;
    grid-column: 1/4;
}
.containerMenu{
    background: #d3eafc;
    grid-row: 2/4;
}
.containerMain{
    background: #d3eafc;
}
.containerRight{
    background: #d3eafc;
}
.conatainerFooter{
    background: #d3eafc;
    grid-column: 2/4;
}
```

## Questão 15
> Crie uma página web conforme o layout abaixo que seja responsiva para ser utilizada nos diferentes navegadores e dispositivos.

```
.layout{
    background: #f1f1f1;
    display: grid;
    grid-gap: 1.5em;
    text-align: center;
}
.container{
    background: #fff;
    border: 1px solid;
}
.containerCD{
    display: grid;
    grid-gap: 1.5em;
    grid-template-columns: auto auto;
}

@media screen and (min-width: 0px) {
    .layout{
        grid-template-rows: 15vh 20vh 15vh 15vh;
    }
}

@media screen and (min-width: 1200px) {
    .layout{
        grid-template-columns: auto auto 35%;
        grid-template-rows: 15vh 20vh 15vh;
    }
    .containerA{
        grid-column: 1/4;
    }
    .containerB{
        grid-column: 1/3;
    }
    .containerCD{
        grid-column: 1/3;
        grid-gap: 1.5em;
    }
    .containerE{
        grid-column: 3/4;
        grid-row: 2/4;
    }
}
```
