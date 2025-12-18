
# Gerenciamento de Estado em Componentes de Função no React

## O que é Gerenciamento de Estado?

O gerenciamento de estado refere-se à maneira como um componente em React mantém e atualiza informações que podem mudar ao longo do tempo.  
Imagine que você tem um termômetro que mostra a temperatura. A temperatura pode mudar, e o termômetro precisa atualizar a leitura para refletir essa mudança.  
No React, usamos algo chamado `useState` para gerenciar essas mudanças de estado dentro de um componente.

---

## Exemplo Prático

Vamos imaginar que você está criando um aplicativo que exibe o nome de um usuário.  
Inicialmente, o nome é **"John"**. Quando o usuário clica em um botão, o nome muda para **"John Doe"**.  
Aqui está como você faria isso usando o `useState`:

```javascript
import React, { useState } from 'react';

function NomeUsuario() {
  // Declarando uma variável de estado chamada 'nome' e uma função para atualizá-la
  const [nome, setNome] = useState('John');

  // Função para atualizar o nome
  const atualizarNome = () => {
    setNome('John Doe');
  };

  return (
    <div>
      <h1>O nome é: {nome}</h1>
      <button onClick={atualizarNome      <button onClick={atualizarNome}>Mudar Nome</button>
    </div>
  );


#Como Funciona?

useState: A função useState é chamada com o valor inicial ('John'). Ela retorna um array com duas partes: o valor atual do estado (nome) e uma função para atualizá-lo (setNome).
Atualização do Estado: Quando o botão é clicado, a função atualizarNome é chamada, que usa setNome para mudar o valor de nome para 'John Doe'. Isso faz com que o componente seja re-renderizado, mostrando o novo nome na tela.


# Entendendo `setName` e `setStateName` no Contexto do React

No React, quando você usa o hook `useState`, ele retorna um array com duas partes:

- **Primeira parte**: o valor atual do estado (por exemplo, `stateName`).
- **Segunda parte**: uma função que você usa para atualizar esse estado (por exemplo, `setStateName`).

---

## Definição das Funções

- **`stateName`**: Este é o valor atual do estado. Ele representa a condição do componente em um determinado momento.  
  Exemplo: se você estiver gerenciando o nome de um usuário, `stateName` pode ser `"John"`.

- **`setStateName`**: Esta é a função que você chama para atualizar o valor do estado.  
  Quando você chama `setStateName` com um novo valor, o React atualiza o estado e re-renderiza o componente para refletir essa mudança.  
  Exemplo: para mudar o nome de `"John"` para `"John Doe"`, você chamaria:

  ```javascript
  setStateName("John Doe");
 
