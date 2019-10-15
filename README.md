# Front End Patterns (Padrões de projeto frontend)

## Nomenclaturas

### JS

- **handle + algumaCoisa**: Função de callback atribuída ao bind de um evento.
- **on + algumaCoisa**: Função chamada para propagar um evento (chamada dentro do "handleAlgumaCoisa").
- **is + algumaCoisa**: Função que verifica algo e retorna um booleano.
- **(passado de qualquer verbo no inglês)**: Booleano indicando se algo já foi feito.

### Classes CSS

#### Estados

- **is-active**
- **is-loading**
- **is-hidden**
- **is-selected**

### API

- **{ message }**: mensagem de sucesso ou erro.
- **{ data }**: demais valores.

## Javascript

- Um componente não sabe a tecnologia do outro.

### Componentes motores

Esses na maioria dos casos não conhecem o lado do cliente, calculam, escutam eventos e fazem chamadas ajax de forma parametrizável, ou seja, prestam serviço mas não sabem para quem.

- Eventos devem ser sempre propagados. Se houver chamar a função de callback correspondente, enviando o evento.
- Parametrizável. Por exemplo, todo bind é feito em um seletor de um valor recebido ou de um valor padrão.

### Componentes mediadores

Trabalham do lado do cliente, são estes que chamam os motores e reagem aos seus retornos. Estes normalmente se expressam de forma visual.

### Componentes de serviços

Um código a parte que que faz processos genéricos, como validações, iterações de array, busca em strings...
