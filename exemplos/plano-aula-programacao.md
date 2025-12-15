# 💻 Plano de Aula: Fundamentos de Programação JavaScript

## 📊 Informações Gerais

| Item | Detalhes |
|------|----------|
| **Disciplina** | Programação / Desenvolvimento Web |
| **Título** | Introdução ao JavaScript: Variáveis, Tipos de Dados e Operadores |
| **Duração** | 90 minutos |
| **Nível** | Iniciante |
| **Público-Alvo** | Estudantes sem experiência prévia em programação |
| **Modalidade** | Híbrida (presencial/online) |

## 🎯 Objetivos de Aprendizagem

### Objetivos Gerais
- Compreender os conceitos fundamentais de programação
- Desenvolver raciocínio lógico computacional
- Criar programas simples em JavaScript

### Objetivos Específicos
Ao final desta aula, o aluno será capaz de:

1. Declarar e utilizar variáveis em JavaScript
2. Identificar e trabalhar com diferentes tipos de dados (string, number, boolean)
3. Aplicar operadores aritméticos, de comparação e lógicos
4. Criar scripts simples para resolver problemas práticos
5. Utilizar o console do navegador para testar código

### Competências Desenvolvidas
- Pensamento computacional
- Resolução de problemas
- Atenção aos detalhes
- Capacidade de depuração

## 📚 Conteúdo Programático

### 1. Introdução ao JavaScript
- Histórico e importância
- Onde o JavaScript é usado
- Primeiro "Hello World"

### 2. Variáveis
- Conceito de variável
- Declaração: `let`, `const`, `var`
- Regras de nomenclatura
- Boas práticas

### 3. Tipos de Dados
- Number (números)
- String (textos)
- Boolean (verdadeiro/falso)
- Undefined e Null
- Typeof

### 4. Operadores
- Aritméticos: +, -, *, /, %, **
- Atribuição: =, +=, -=, *=, /=
- Comparação: ==, ===, !=, !==, >, <, >=, <=
- Lógicos: &&, ||, !

## 🛠️ Metodologia

### Estratégias de Ensino
- **Expositiva dialógica**: Explicação com participação ativa
- **Demonstração prática**: Live coding
- **Aprendizagem por descoberta**: Exercícios guiados
- **Peer programming**: Programação em duplas

### Recursos Didáticos
- Editor de código (VS Code ou similar)
- Navegador web (Chrome/Firefox)
- Console do desenvolvedor
- Apresentação de slides
- Exercícios práticos
- Repositório GitHub com exemplos

## ⏱️ Desenvolvimento da Aula

### 1ª Etapa: Introdução e Contextualização (15 min)

**Atividade de Abertura**
- Apresentação do tema
- Discussão: "Onde vocês veem JavaScript no dia a dia?"
- Demonstração: Sites e aplicações que usam JS

**Primeiro Contato**
```javascript
// Primeiro programa
console.log("Olá, Mundo!");
```

### 2ª Etapa: Variáveis (20 min)

**Explicação Teórica** (8 min)
- O que é uma variável
- Por que usar variáveis
- Diferenças entre let, const e var

**Demonstração Prática** (12 min)
```javascript
// Declarando variáveis
let nome = "Maria";
let idade = 25;
const PI = 3.14159;

console.log("Nome:", nome);
console.log("Idade:", idade);
console.log("PI:", PI);

// Modificando variáveis
nome = "João";
idade = 30;
// PI = 3.14; // Erro! const não pode ser reatribuído
```

**Exercício Guiado**
- Criar variáveis para nome, sobrenome e idade
- Exibir no console

### 3ª Etapa: Tipos de Dados (20 min)

**Exploração dos Tipos** (10 min)
```javascript
// Numbers (números)
let inteiro = 42;
let decimal = 3.14;
let negativo = -10;

// Strings (textos)
let saudacao = "Olá";
let nome = 'JavaScript';
let frase = `Bem-vindo ao ${nome}!`; // Template string

// Boolean (lógico)
let estaChovendo = true;
let temSol = false;

// Verificando tipos
console.log(typeof inteiro);    // "number"
console.log(typeof saudacao);   // "string"
console.log(typeof estaChovendo); // "boolean"
```

**Atividade Prática** (10 min)
Criar um "cartão de apresentação" digital:
```javascript
let nome = "Seu Nome";
let profissao = "Estudante de Programação";
let idade = 20;
let gostaDeProgramar = true;

console.log("=== CARTÃO DE APRESENTAÇÃO ===");
console.log("Nome:", nome);
console.log("Profissão:", profissao);
console.log("Idade:", idade);
console.log("Gosta de programar?", gostaDeProgramar);
```

### 4ª Etapa: Operadores (25 min)

**Operadores Aritméticos** (8 min)
```javascript
let a = 10;
let b = 3;

console.log("Soma:", a + b);           // 13
console.log("Subtração:", a - b);      // 7
console.log("Multiplicação:", a * b);  // 30
console.log("Divisão:", a / b);         // 3.333...
console.log("Resto:", a % b);           // 1
console.log("Potência:", a ** b);       // 1000
```

**Operadores de Comparação** (8 min)
```javascript
let x = 5;
let y = "5";

console.log(x == y);   // true (compara valor)
console.log(x === y);  // false (compara valor E tipo)
console.log(x != y);   // false
console.log(x !== y);  // true
console.log(x > 3);    // true
console.log(x <= 5);   // true
```

**Operadores Lógicos** (9 min)
```javascript
let temChuva = true;
let temGuarda = false;

// AND (&&) - Todas condições devem ser verdadeiras
console.log(temChuva && temGuarda); // false

// OR (||) - Pelo menos uma condição deve ser verdadeira
console.log(temChuva || temGuarda); // true

// NOT (!) - Inverte o valor
console.log(!temChuva); // false
```

**Desafio Prático**
Calculadora simples:
```javascript
let num1 = 15;
let num2 = 4;

console.log("=== CALCULADORA ===");
console.log(`${num1} + ${num2} = ${num1 + num2}`);
console.log(`${num1} - ${num2} = ${num1 - num2}`);
console.log(`${num1} * ${num2} = ${num1 * num2}`);
console.log(`${num1} / ${num2} = ${num1 / num2}`);
```

### 5ª Etapa: Prática Integrada (10 min)

**Projeto: Sistema de Loja Simples**
```javascript
// Dados do produto
const nomeProduto = "Notebook";
const precoUnitario = 2500;
const quantidade = 2;
const desconto = 0.10; // 10%

// Cálculos
const subtotal = precoUnitario * quantidade;
const valorDesconto = subtotal * desconto;
const total = subtotal - valorDesconto;

// Resultado
console.log("=== NOTA FISCAL ===");
console.log("Produto:", nomeProduto);
console.log("Preço unitário: R$", precoUnitario);
console.log("Quantidade:", quantidade);
console.log("Subtotal: R$", subtotal);
console.log("Desconto (10%): R$", valorDesconto);
console.log("TOTAL: R$", total);
```

## 🎯 Avaliação

### Avaliação Formativa

**Durante a Aula**
- Observação da participação
- Resolução dos exercícios guiados
- Questões e dúvidas
- Compartilhamento de soluções

### Exercício Final (Para Casa)

**Desafio: Conversor de Temperatura**

Criar um programa que:
1. Declare uma temperatura em Celsius
2. Converta para Fahrenheit usando a fórmula: `F = (C * 9/5) + 32`
3. Converta para Kelvin usando: `K = C + 273.15`
4. Exiba os resultados formatados

**Solução Esperada**
```javascript
const celsius = 25;
const fahrenheit = (celsius * 9/5) + 32;
const kelvin = celsius + 273.15;

console.log("=== CONVERSOR DE TEMPERATURA ===");
console.log(`${celsius}°C`);
console.log(`${fahrenheit}°F`);
console.log(`${kelvin}K`);
```

### Critérios de Avaliação

| Critério | Peso |
|----------|------|
| Corretude do código | 40% |
| Uso adequado de variáveis | 20% |
| Clareza e organização | 20% |
| Criatividade na apresentação | 20% |

## 📚 Recursos Complementares

### Materiais de Apoio
- [MDN JavaScript Guide](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide)
- [JavaScript.info](https://javascript.info/)
- [FreeCodeCamp JavaScript](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/)

### Ferramentas Online
- [CodePen](https://codepen.io/) - Editor online
- [JSFiddle](https://jsfiddle.net/) - Testar código rapidamente
- [Repl.it](https://replit.com/) - Ambiente de desenvolvimento online

### Vídeos Recomendados
- "JavaScript para Iniciantes" - Curso em Vídeo
- "Variáveis e Tipos de Dados" - Rocketseat

## 🔄 Próximos Passos

### Próxima Aula
- Estruturas condicionais (if/else)
- Switch case
- Operador ternário

### Roadmap do Curso
1. ✅ Fundamentos (variáveis, tipos, operadores)
2. ⏳ Estruturas de controle
3. ⏳ Funções
4. ⏳ Arrays e objetos
5. ⏳ DOM e eventos
6. ⏳ Assincronismo

## 📝 Observações do Professor

### Pontos de Atenção
- Alunos podem confundir `=` (atribuição) com `==` (comparação)
- Enfatizar a diferença entre `==` e `===`
- Explicar bem o conceito de `const` vs `let`
- Reservar tempo para dúvidas sobre nomenclatura de variáveis

### Adaptações Possíveis
- **Para turmas mais avançadas**: Incluir destructuring e spread operator
- **Para turmas com dificuldade**: Focar apenas em let e const, deixar var para depois
- **Modalidade online**: Usar breakout rooms para exercícios em grupo

### Dicas de Engajamento
- Usar exemplos do cotidiano (calculadora, conversor)
- Incentivar os alunos a testarem variações do código
- Promover "code review" entre colegas
- Criar um repositório compartilhado para soluções

## ✅ Checklist do Professor

**Antes da Aula**
- [ ] Testar todos os exemplos de código
- [ ] Preparar ambiente de desenvolvimento
- [ ] Disponibilizar links e materiais
- [ ] Criar repositório com códigos de exemplo

**Durante a Aula**
- [ ] Compartilhar tela para demonstrações
- [ ] Alternar entre teoria e prática
- [ ] Fazer pausas para dúvidas
- [ ] Registrar dúvidas frequentes

**Após a Aula**
- [ ] Disponibilizar códigos no GitHub
- [ ] Enviar exercícios para casa
- [ ] Responder dúvidas no fórum/chat
- [ ] Preparar feedback individualizado

---

📌 **Observação**: Este plano de aula foi criado utilizando metodologia de design instrucional e ferramentas de IA para personalização do conteúdo.