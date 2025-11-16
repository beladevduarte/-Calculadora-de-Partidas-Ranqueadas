# 🏆 Calculadora de Partidas Rankeadas

![Status](https://img.shields.io/badge/Status-Concluído-00C853?style=for-the-badge)
![JavaScript](https://img.shields.io/badge/Linguagem-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![DIO](https://img.shields.io/badge/Projeto-DIO-7A1CAC?style=for-the-badge)
![Lógica](https://img.shields.io/badge/Nível-Iniciante%20%2F%20Intermediário-4CAF50?style=for-the-badge)

---

## ✨ Entendendo o Desafio

Agora é a sua hora de brilhar e construir um perfil de destaque na **DIO**!  
Este projeto faz parte da formação e foi desenvolvido para reforçar conceitos essenciais de lógica de programação.

Aqui você vai praticar e demonstrar domínio sobre:

- Variáveis
- Operadores
- Estruturas de decisão (if/else)
- Laços de repetição
- Funções
- Organização e clareza de código

Tudo isso compondo um projeto simples e direto, mas extremamente útil para quem está evoluindo na programação.

---

## 🎯 Objetivo do Projeto

Criar uma função que:

1. Recebe como parâmetros:
   - quantidade de vitórias  
   - quantidade de derrotas  

2. Calcula o **saldo de Rankeadas** através da fórmula:

3. Classifica o jogador conforme o número total de vitórias.

4. Retorna a mensagem final:

---

 ##  "O Herói tem de saldo de {saldoVitorias} está no nível de {nivel}"

## 🏅 Classificação por Vitórias

| Vitórias | Nível |
|---------|--------|
| 0–10 | 🪨 Ferro |
| 11–20 | 🥉 Bronze |
| 21–50 | 🥈 Prata |
| 51–80 | 🥇 Ouro |
| 81–90 | 💎 Diamante |
| 91–100 | 🔥 Lendário |
| 101+ | 🐉 Imortal |

---

## 🔥 Lógica Aplicada

A classificação não é baseada no saldo, e sim no número **total de vitórias**.

O saldo serve apenas para retornar na mensagem final.

A lógica completa está estruturada em condicionais encadeadas:

```javascript
if (vitorias < 10) {
  nivel = "Ferro";
} else if (vitorias <= 20) {
  nivel = "Bronze";
} else if (vitorias <= 50) {
  nivel = "Prata";
} else if (vitorias <= 80) {
  nivel = "Ouro";
} else if (vitorias <= 90) {
  nivel = "Diamante";
} else if (vitorias <= 100) {
  nivel = "Lendário";
} else {
  nivel = "Imortal";
}

````


💻 Código Completo

````javascript
function calcularNivel(vitorias, derrotas) {
  let saldoVitorias = vitorias - derrotas;
  let nivel = "";

  if (vitorias < 10) {
    nivel = "Ferro";
  } else if (vitorias <= 20) {
    nivel = "Bronze";
  } else if (vitorias <= 50) {
    nivel = "Prata";
  } else if (vitorias <= 80) {
    nivel = "Ouro";
  } else if (vitorias <= 90) {
    nivel = "Diamante";
  } else if (vitorias <= 100) {
    nivel = "Lendário";
  } else {
    nivel = "Imortal";
  }

  return `O Herói tem de saldo de ${saldoVitorias} está no nível de ${nivel}`;
}

console.log(calcularNivel(75, 20));
