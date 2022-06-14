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

Afim de uma melhor preparação do conteúdo, algumas definições metas são indispensáveis no head do documento, como a biblioteca de caracteres e *viewport* da tela em que a página será carregada, além da indicação sobre a lingua em que o conteúdo mostrado apresentada. Vale ressaltar que a falta destes não afeta na construção do *site*, mas o torna melhor definido e, assim, evitar erros de apresentação.

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

O trecho de codigo anterior seleciona as tags de título do HTML e os atribui. Contudo, pensando num projeto onde nem todo conteúdo dessas tags precisam destas transformações, o método da criação de classe também seria válido.

```
.containerCabecalho{
    font-family: Arial;
    font-weight: bold;
    text-transform: uppercase;
}
```

Assim, para os cabeçalhos que precisam estar definidos com fonte Arial, devem estar em negrito e em caixa alta, basta adicionar a classe `containerCabecalho` e terá o mesmo resultado.

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

## Questão 7
> Um dos critérios de um determinado projeto é que todos os links devem ficar sublinhados quando o usuário passar o mouse por cima deles. Escreva o código para garantir essa regra. 

## Questão 8
> Escreva um comando JavaScript onde o texto Hello World! seja exibido no console do navegador através de uma variável.

## Questão 9
> Usando o mesmo código da questão anterior, substitua o texto que será exibido no console do navegador para Hello Toodoo! O novo valor deve sobrescrever o valor original.

## Questão 10
> Desenvolva via JavaScript a seguinte estrutura de código levando em consideração as seguintes regras:
>> a) Uma variável deve ter o nome de sorvete de chocolate;
>> b) Se o seu valor for igual a chocolate, deve ser exibido no alerta do navegador a mensagem: Amo sorvete de chocolate;
>> c) Se o seu valor for outro, deve exibir a mensagem: Prefiro outros sabores.

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

## Questão 11 (2)
> Em CSS existe uma maneira de sobrescrever um estilo, quando não há outra maneira, além dessa, de se fazer isso. Qual das propriedades a seguir é utilizada para isso? 

(a) force
(b) strong
(c) !important
(d) nenhuma das alternativas

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
(a) red
(b) blue
(c) green
(d) black

## Questão 13
> Levando em consideração a semântica de código, escreva o HTML de uma tabela que possui as seguintes características:
>> a) Deve possuir 3 colunas (Nome, Idade, Gênero);
>> b) Deve possuir 2 linhas (com dados fictícios);
>> c) E uma última linha com todas as suas colunas mescladas.

## Questão 14
> Utilizando grid system, não sendo necessário a responsividade, elabore uma página web que siga o layout indicado.

## Questão 15
> Crie uma página web conforme o layout abaixo que seja responsiva para ser utilizada nos diferentes navegadores e dispositivos.
