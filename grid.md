# CSS - GRID

O CSS Grid Layout é um sistema de layout bidimensional que permite criar designs complexos de maneira mais simples e intuitiva.

### 1. display
Define um contêiner como um contêiner de grid.
```css
.container {
    display: grid;
}
```

### 2. `grid-template-columns` e `grid-template-rows`
Define o número de colunas e linhas no grid e seus tamanhos.

```css
.container {
    display: grid;
    grid-template-columns: 100px 200px 100px; /* 3 colunas */
    grid-template-rows: 100px 200px; /* 2 linhas */
}
```

### 3. `grid-column-gap`, `grid-row-gap` e `gap`
Define o espaçamento entre as colunas, linhas ou ambos.

```css
.container {
    display: grid;
    gap: 10px; /* Espaço de 10px entre colunas e linhas */
    grid-column-gap: 10px; /* Apenas entre colunas */
    grid-row-gap: 15px; /* Apenas entre linhas */
}
```

### 4. `grid-template-areas`
Define áreas nomeadas no grid para facilitar o posicionamento de elementos.

```css
.container {
    display: grid;
    grid-template-areas: 
        "header header header"
        "sidebar content content"
        "footer footer footer";
    grid-template-columns: 1fr 2fr 1fr;
    grid-template-rows: auto;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }
.footer { grid-area: footer; }
```

### 5. `grid-area`
Associa um item do grid a uma área nomeada.

```css
.item1 {
    grid-area: header;
}
```

### 6. `grid-column` e `grid-row`
Define a posição de um item do grid em termos de linhas e colunas.

```css
.item {
    grid-column: 3; /* Posiciona o item na coluna 3 */
    grid-row: 2; /* Posiciona o item na linha 2 */
}
```

### 7. `justify-items` e `align-items`
Alinha os itens dentro das células do grid horizontalmente e verticalmente, respectivamente.

```css
.container {
    display: grid;
    justify-items: center; /* Centraliza horizontalmente */
    align-items: center; /* Centraliza verticalmente */
}
```

### 8. `justify-content` e `align-content`
Alinha o próprio grid dentro do contêiner, horizontalmente e verticalmente, respectivamente.

```css
.container {
    display: grid;
    justify-content: center; /* Centraliza o grid no contêiner */
    align-content: center; /* Centraliza o grid verticalmente no contêiner */
}
```

### 9. `grid-auto-flow`
Controla como os itens do grid são colocados automaticamente.

```css
.container {
    display: grid;
    grid-auto-flow: row; /* Padrão, preenche por linhas */
    /* Outras opções: column, dense, row dense, column dense */
}
```

- **`row`**: Padrão. Coloca os itens do grid em ordem de linha, da esquerda para a direita.
- **`column`**: Coloca os itens do grid em ordem de coluna, de cima para baixo.
- **`dense`**: Tenta preencher todas as lacunas no grid com itens subsequentes que se ajustem, evitando espaços vazios.
- **`row dense`**: Combina a ordenação por linhas com o comportamento `dense`, preenchendo lacunas enquanto segue a ordem de linhas.
- **`column dense`**: Combina a ordenação por colunas com o comportamento `dense`, preenchendo lacunas enquanto segue a ordem de colunas.

### 10. `grid-auto-rows` e `grid-auto-columns`
Define o tamanho das linhas e colunas geradas automaticamente.

```css
.container {
    display: grid;
    grid-auto-rows: 100px; /* Altura das linhas automáticas */
    grid-auto-columns: 100px; /* Largura das colunas automáticas */
}
```

Essas são as propriedades essenciais do CSS Grid. Com essas propriedades, você pode criar layouts complexos de maneira eficiente e com um controle preciso sobre o posicionamento e alinhamento dos elementos.