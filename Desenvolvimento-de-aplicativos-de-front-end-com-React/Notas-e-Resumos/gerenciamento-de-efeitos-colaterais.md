# Gerenciamento de Efeitos Colaterais e Hooks Personalizados

Gerenciamento de efeitos colaterais e o uso de hooks personalizados no React, com foco na utilização do hook UseEffect.

## Uso do UseEffect
- O UseEffect é um hook do React que permite executar efeitos colaterais em componentes funcionais, como buscar dados de uma API ou manipular o DOM.
- Os efeitos colaterais são ações assíncronas que afetam o estado da aplicação ou a interface do usuário.

## Dependências do UseEffect
- As dependências são variáveis que determinam quando o UseEffect deve ser executado. Um array vazio faz com que o efeito execute apenas uma vez, enquanto incluir variáveis faz com que o efeito execute sempre que essas variáveis mudarem.
- Se não houver array de dependências, o efeito será executado após cada renderização do componente.

## Hooks Personalizados
- Hooks personalizados permitem abstrair lógica complexa para reutilização em diferentes componentes.
- Um exemplo é o hook UseToggle, que gerencia o estado de um botão que alterna entre verdadeiro e falso, facilitando a implementação de funcionalidades reutilizáveis.

## Conceito de "UseEffect" e "Side Effects"

O "UseEffect" é uma ferramenta que usamos em React para realizar ações que acontecem fora do nosso componente, como buscar dados de uma API ou manipular a interface do usuário. Imagine que você está organizando uma festa. O "UseEffect" seria como a lista de tarefas que você precisa fazer assim que a festa começa, como acender as luzes ou tocar música. Essas tarefas são chamadas de "Side Effects" (efeitos colaterais) porque elas afetam o que as pessoas veem e sentem na festa, assim como as ações que o "UseEffect" realiza afetam a interface do seu aplicativo.

Por exemplo, se você tem um aplicativo que mostra uma lista de comidas, o "UseEffect" pode ser usado para buscar essa lista de um site assim que o aplicativo é aberto. Assim que os dados são recebidos, eles são exibidos na tela. Isso acontece de forma automática, sem que você precise fazer isso manualmente toda vez. Você pode pensar nisso como um assistente que cuida de tudo para você, permitindo que você se concentre em aproveitar a festa!

O **UseEffect** é como um assistente que ajuda a realizar tarefas assim que um componente é carregado, como buscar dados de uma API ou manipular o DOM. Imagine que você está organizando uma festa. Assim que os convidados chegam (o componente é montado), você precisa preparar algumas coisas, como colocar a música para tocar ou servir os aperitivos (executar efeitos colaterais). O UseEffect faz exatamente isso!

### Exemplo Prático

Aqui está um exemplo simples de como usar o UseEffect para buscar uma lista de itens de comida de uma API:

```javascript
import React, { useState, useEffect } from 'react';

function FoodList() {
  const [foods, setFoods] = useState([]);

  useEffect(() => {
    fetch('https://api.example.com/foods')
      .then(response => response.json())
      .then(data => setFoods(data))
      .catch(error => console.error('Erro ao buscar dados:', error));
  }, []); // O array vazio significa que isso só será executado uma vez, quando o componente for montado.

  return (
    <ul>
      {foods.map(food => (
        <li key={food.id}>{food.name}</li>
      ))}
    </ul>
  );
}

export default FoodList;
```

Neste código:
- **useState** é usado para criar uma variável de estado chamada `foods`, que começa como um array vazio.
- **useEffect** é chamado para buscar dados da API assim que o componente é montado. O array vazio `[]` como segundo argumento significa que essa busca só acontece uma vez.
- Quando os dados são recebidos, eles são convertidos em JSON e armazenados na variável de estado `foods` usando `setFoods`.


## Perguntas Teste

1. **Verdadeiro/Falso:** O "UseEffect" é usado para realizar efeitos colaterais em componentes funcionais no React.
   - **R:** V

2. **Múltipla Escolha:** Qual das seguintes opções é um exemplo de um efeito colateral que pode ser gerenciado pelo "UseEffect"?
   - A) Definir uma variável de estado
   - B) Buscar dados de uma API **(CERTA)**
   - C) Renderizar um componente
   - D) Criar um novo componente

3. **Aberta:** Explique como o "UseEffect" pode ser utilizado para buscar dados de uma API e atualizar o estado de um componente.
   - **R:** O UseEffect pode ser utilizado para buscar dados de uma API ao fazer uma requisição dentro do hook, e quando os dados são recebidos, você pode usar a função de atualização de estado, como `setFoods`, para armazenar esses dados no estado do componente.

4. **Aberta:** O que acontece se você passar um array vazio como segundo argumento para o "UseEffect"?
   - **R:** Significa que a busca de dados na API só acontece uma vez (quando o componente é montado).

5. **Verdadeiro/Falso:** Se você não fornecer um array de dependências para o "UseEffect", ele será executado apenas uma vez quando o componente for montado.
   - **R:** F