# Aula de introdução ao CSS
Neste repositório, você encontrará todos os arquivos gerados durante a aula. Abaixo, disponibilizamos imagens demonstrativas para facilitar o entendimento de algumas estilizações.


## Diferenças de Box Sizing

O `box-sizing` é uma propriedade CSS que define como o cálculo da largura e altura de um elemento deve ser feito.

### `content-box` (padrão)
- **Descrição**: A largura e altura são aplicadas somente ao conteúdo do elemento. O padding e a borda são adicionados à largura e altura total.
- **Exemplo**: Se um elemento tem `width: 100px` e `border: 10px`, a largura total será `100px + 20px = 120px`.

### `border-box`
- **Descrição**: A largura e altura incluem o conteúdo, o padding e a borda. Isso facilita o controle do layout, pois a largura total do elemento é sempre a mesma, independentemente da borda e do padding.
- **Exemplo**: Se um elemento tem `width: 100px` e `border: 10px`, a largura total permanece `100px`.

### Exemplo em CSS
```css
/* Padrão (content-box) */
.element {
    box-sizing: content-box;
}

/* Border-box */
.element-border-box {
    box-sizing: border-box;
}
```

![Box sizing](/assets/box-sizing.png)

## Centralização Horizontal de Elementos Utilizando `margin`
```css
.elemento {
 margin: 0 auto;   
}
```

## Centralização de Elementos Utilizando `position`

Centralizar elementos em CSS pode ser feito de várias maneiras, e uma delas é utilizando a propriedade `position`. Aqui estão algumas abordagens comuns:

### Centralização Horizontal com `position: absolute`
Para centralizar um elemento horizontalmente dentro de um contêiner pai, você pode usar `position: absolute` junto com as propriedades `left` e `transform`.

```css
.parent {
    position: relative; /* O contêiner pai deve ter posição relativa ou absoluta */
}

.child {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
}
```

![Imagem da posição com translate](/assets/image.png)