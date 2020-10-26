# Juni - Teste Animale

## Estrutura do Rodapé Em HTML

[Organograma do Código HTML](https://whimsical.com/embed/H8xjMLif1GLHBTZzA9Ex1u)

[Ver Código Em HTML Aqui](https://github.com/rmkarato/juni/blob/main/code/teste-juni-estrutura.html)

## Script - Rodapé Fixo

[Script Para Rodar No Console do Navegador](https://github.com/rmkarato/juni/blob/main/code/teste-juni-console-animale.txt)

- Copiar e colar o scrip acima no console do navegador.

## Tasklist

- [x] Colocar o rodapé fixo no fim da página;
- [x] Injetar o CSS via Javascript;
- [x] Script funcionando em qualquer página de produto;
- [x] Pegar imagem em miniatura de forma dinâmica;
- [x] Pegar nome do produto de forma dinâmica;
- [x] Pegar valor do produto de forma dinâmica;
- [x] Calcular desconto de 10% sobre o produto;
- [x] Implantar o botão de "adicionar à sacola";
- [ ] Botão "adicionar à sacola" funcionando;
- [x] Implantar o botão "X" para fechar rodapé;
- [x] Botão "x" funcionando;

## Observação

- Após fechar o rodapé, ele pode ser aberto através da função "openFooterProduct" implantada.

> openFooterProduct();

### Como criei o rodapé?

- Selecionei o footer já existente através da tag "querySelector()";
- Criei os elementos novos que contém [no meu código HTML](http://google.com/) - com a tag "createElement()";
- Através do "appendChild()" eu conectei o código HTML, fazendo com que os respectivos elementos filhos ficassem ligados aos elemento-pai;
- Com o "textContent", nomeei com informações genéricas os elementos;
- Comecei a criar alguns estilos chamando o elemento com ".style". Assim pude ver como ía ficar a estrutura do rodapé;
- Analisando o código existente, peguei algumas classes que eu poderia reaproveitar, com o ".className" - assim pude pegar algumas estilizações, como a do botão "adicionar à sacola";
- Com o ".setAttribute" e mais ".style", fui configurando o CSS dos elementos, até chegar da forma que foi pedido.

### Como peguei a imagem do produto?

- Através do "querySelector()" e do "getAttribute()", peguei o "src" e o "alt" da imagem principal do produto;
- Então atribuí este "src" e este "alt" ao elemento novo que criei (productImg).

### Como peguei o nome do produto?

- Através do "querySelector()" e do ".innerHTML", peguei o nome do produto no código existente;
- Então atribuí este ".innerHTML" ao elemento novo que criei (productName).

### Como peguei o preço do produto?

- Através do "querySelector()" e do ".innerHTML", peguei o preço do produto no código existente;
- Então atribuí este ".innerHTML" ao elemento novo que criei (productPriceStr).

### Como peguei o preço do produto com 10% de desconto?

- Para fazer este cálculo, não foi possível utilizar o "querySelector()" e o ".innerHTML", pois o valor vinha como string e junto com o cifrão R$;
- Então acessei o "dataLayer[0]" e peguei o valor através dele;
- Como o dataLayer já devolve o valor como Number, só foi necessário multiplicá-lo por 0.9;
- Com o ".toLocaleString", formatei o valor devolvido na multiplicação com a moeda brasileira;
- Assim o valor aparece do jeito desejado, com cifrão e o ponto entre os milhares (ex. R$ 1.000,00).

## Para fechar o footer através do "X"

- O display inicial do footer está configurado como "display: block";
- Assim, implantei uma função que, quando apertar o "X", transforma em "display: none" e também diminui o height do footer para que fique com o tamanho do original;
- Também foi implantada a função para reabrir o footer. Então o display volta a ficar "block" e o height do footer é aumentado para que ele fique localizado fixo no fim da página.

## Testes

### Zoom 100%
![](https://github.com/rmkarato/juni/blob/main/imgs/rodape-implantado-1.png?w=512)
(rodapé situado no fim da página)

### Zoom 150%
![](https://github.com/rmkarato/juni/blob/main/imgs/rodape-implantado-2.png?w=512)
(preocupação em alinhar a imagem com as miniaturas existentes e também alinhar o botão "adicionar à sacola" com o existente)

### Zoom 75%
![](https://github.com/rmkarato/juni/blob/main/imgs/rodape-implantado-3.png?w=512)
(proporção mantida mesmo com zoom menor)

## Contato

Renata Mitsue Karato

11 9 9763-7438

[Github](https://github.com/rmkarato) | [Linkedin](https://www.linkedin.com/in/rmkarato/)

