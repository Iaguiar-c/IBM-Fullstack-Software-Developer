# Uso de Componentes Funcionais em React

O conteúdo aborda o uso de componentes funcionais em React, focando em props e manipulação de eventos.

## Entendendo Props

- Props são propriedades que permitem passar dados de um componente pai para um componente filho, funcionando como um objeto que armazena atributos.
- As props são imutáveis, ou seja, não podem ser alteradas dentro do componente filho.

## Uso de Props em Componentes

- O componente `App` passa dados para o componente `EmployeeData`, onde as props são acessadas usando a notação de ponto.
- É possível definir valores padrão para as props, garantindo que o componente tenha valores consistentes mesmo que não sejam fornecidos pelo componente pai.

## Princípios e Manipulação de Eventos

- Os princípios das props incluem reutilização, fluxo unidirecional de dados, personalização e composição de componentes.
- A manipulação de eventos é exemplificada com o uso do hook `useState` para controlar a exibição de informações com base em interações do usuário.

### O que são Props?
Props, ou propriedades, são como pacotes de informações que você pode enviar de um componente pai para um componente filho. Imagine que você está enviando uma carta (o componente pai) para um amigo (o componente filho). Na carta, você pode incluir informações como o nome do seu amigo, o que ele gosta, ou qualquer outra coisa que você queira que ele saiba. No React, essas informações são passadas como props.

### Exemplo de Código
Aqui está um exemplo simples para ilustrar como as props funcionam:

### Explicação do Código:
- No componente `App`, estamos chamando o componente `EmployeeData` e passando duas props: `name` e `dept_name`.
- No componente `EmployeeData`, usamos `props` para acessar essas informações. Com `props.name`, conseguimos mostrar o nome "John" e com `props.dept_name`, mostramos "Human Resources".

### Resumo
- **Props** são usadas para passar dados de um componente pai para um componente filho.
- Você pode acessar essas props no componente filho usando `props.nomeDaProp`.

```javascript
// Componente Pai
function App() {
  return (
    <div>
      <EmployeeData name="John" dept_name="Human Resources" />
    </div>
  );
}

// Componente Filho
function EmployeeData(props) {
  return (
    <div>
      <h1>Nome: {props.name}</h1>
      <h2>Departamento: {props.dept_name}</h2>
    </div>
  );
}