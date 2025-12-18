
# Fases do Ciclo de Vida de um Componente Funcional no React

Os componentes funcionais no React são como blocos de construção de uma casa: eles ajudam a criar a interface do usuário.  
O ciclo de vida de um componente funcional passa por **quatro fases principais**:

---

## 1. Fase de Montagem
Imagine que você está montando um quebra-cabeça.  
Primeiro, você organiza as peças (**inicialização**), depois coloca algumas delas no lugar (**inicialização do estado**) e, por fim, faz ajustes para que tudo funcione bem (**efeitos colaterais**).  

Exemplo: você pode usar o `useState` para criar uma variável que conta quantas peças você já montou.

---

## 2. Fase de Atualização
Agora, pense que você está jogando um jogo e precisa atualizar sua pontuação.  
Quando algo muda, como clicar em um botão para aumentar a pontuação, o React reavalia o que deve ser mostrado na tela.  
Isso garante que a interface do usuário esteja sempre atualizada com as informações mais recentes.

---

## 3. Fase de Desmontagem
Quando você termina de jogar e precisa guardar o jogo, é hora de limpar tudo.  
O React faz algo semelhante ao **remover um componente da tela**, garantindo que não haja resíduos, como ouvintes de eventos ou temporizadores, que possam causar problemas mais tarde.

---

## 4. Tratamento de Erros
Se algo der errado, como um erro no jogo, o React tem um plano de emergência.  
Ele usa **limites de erro** (*error boundaries*) para capturar esses problemas e mostrar uma mensagem amigável, em vez de deixar o jogo travar.

---

Essas fases ajudam a garantir que os componentes funcionais funcionem de maneira eficiente e sem problemas.

💡 Se você tiver mais perguntas ou precisar de explicações sobre outros conceitos, estou aqui para ajudar!
``

  
# Exemplo Prático: Ciclo de Vida em Componentes Funcionais no React

Vamos explorar um exemplo prático relacionado ao ciclo de vida de componentes funcionais no React.  
Este exemplo ilustra as fases de **montagem**, **atualização** e **desmontagem**, juntamente com o código correspondente.

---

## 🧪 Exemplo: Contador com Efeitos Colaterais

Neste exemplo, criaremos um componente funcional que implementa um contador.  
O contador será incrementado quando um botão for clicado e exibirá uma mensagem no console quando o componente for desmontado.

### Código:

```javascript
import React, { useState, useEffect } from 'react';

const Contador = () => {
  // Fase de montagem: inicializando o estado
  const [count, setCount] = useState(0);

  // Fase de montagem: usando useEffect para simular um efeito colateral
  useEffect(() => {
    console.log('Componente montado!');

    // Função de limpeza para a fase de desmontagem
    return () => {
      console.log('Componente desmontado!');
    };
  }, []); // O array vazio garante que o efeito só execute uma vez

  // Fase de atualização: função para incrementar o contador
  const incrementar = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <h1>Contador: {count}</h1>
           <button onClick={incrementar}>Incrementar</button>
    </div>
  );
};



## 🔍 Explicação do Código

### ✅ Fase de Montagem
- Usamos **`useState`** para inicializar o estado `count` com o valor `0`.
- O **`useEffect`** é utilizado para simular um efeito colateral, como um log no console quando o componente é montado.
- O retorno da função dentro do `useEffect` é chamado na desmontagem, permitindo executar qualquer limpeza necessária.

---

### 🔄 Fase de Atualização
- A função **`incrementar`** é chamada quando o botão é clicado.
- Ela atualiza o estado `count`, provocando uma **re-renderização** do componente e exibindo o novo valor do contador.

---

### 🗑️ Fase de Desmontagem
- Quando o componente é removido do DOM, a função de limpeza dentro do `useEffect` é executada.
- Isso permite **remover ouvintes de eventos**, **cancelar assinaturas** ou **liberar recursos**.
``
