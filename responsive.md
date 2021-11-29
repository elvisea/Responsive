# Responsividade

## CSS Units - Unidades de medidas do CSS

### Layout Fixo:

Pixel
```css
px
```

### Layout Fluido: 

Porcentagem
```css
%
```

Auto
```css
auto
```

Viewport Height
```css
vh
```

Viewport Width
```css
vw
```

Estratégia:  

Trabalhar com `max-width` e `width` juntas.

### Equivalencias:

```css
1px = 0.75pt
```

```css
16px = 12pt
```

### Textos Fluidos

Multiplicado pelo elemento pai:
```css
em
```

Multiplicado pelo root:
```css
rem
```

Estratégia:

Mudar `font-size` do root para `%`.  
Então toda vez que ele mudar todo o restante abaixo dele será mudado.  
Neste caso mudamos para `62.5%` para que cada `1rem` seja considerado `10px`. 

Primeira etapa
```css
html {
  font-size: 62.5%;
}
```

Segunda etapa
```css
.suaClasse {
  font-size: 1.6rem:
}
```

Terceira etapa.
```bash
Mudar font-size e line-height de `px` para `rem`
```

Dentro da tag `Head` do `Html` deve conter a tag `Meta` com as seguintes propriedades: 
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Usar Media Queries. Exemplo:

```css
@media (max-width: 768px){
  font-size: 50%;
}
```

Usar Display Grid com colunas flexíveis. Exemplo:  

```css
.suaClasse {
  display: grid;
  grid-template-columns: 1fr, 1fr, 1fr;
}
```

Ou usar com `repeat`. Exemplo: 

```css
.suaClasse {
  display: grid;
  grid-template-columns: repeat(3, minmax(250px, 1fr));
}
```

Ou usar com `auto-fit`. Exemplo: 

```css
.suaClasse {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
}
```

Usar propriedade `order: -1` para inverter a ordem dos elementos.Exemplo: 

```css
.suaClasse {
  order: -1;
}
```