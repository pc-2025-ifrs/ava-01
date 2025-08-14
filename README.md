# Atividade Avaliada 01: implementar observando os casos excepcionais

1.0 pt, checkpoint em 20/08, prazo até 24/08

Considere duas funções, para calcular o MMC (Mínimo Múltiplo Comum) e MDC (Máximo Divisor Comum), por exemplo:

```js
function mmc(n1, n2) {
    // implementação ...
}
```

Implementar o _caminho feliz_ sendo que as chamadas a seguir funcionem:

```js
console.log(mmc(3, 4)) // 12
console.log(mmc(18, 131)) // 2358 https://www.wolframalpha.com/input?i=lcm%2818%2C+131%29
// também para inteiros negativos (a resposta é sempre positiva)
console.log(mmc(-3, -4)) // 12 https://www.wolframalpha.com/input?i=lcm%28-3%2C+-4%29
console.log(mmc(-5, 16)) // 80 https://www.wolframalpha.com/input?i=lcm%28-5%2C+16%29
```

Pensar em quais seriam os retornos para os casos excepcionais (chamadas inválidas), por exemplo:

```js
// decimais não são computáveis
console.log(mmc(3.5, 4)) // ?
console.log(mmc(3, 4.1)) // ?
console.log(mmc(3.8, 4.1)) // ?
// não números
console.log(mmc('3', '4')) // ?
console.log(mmc('a', 'b')) // ?
console.log(mmc([3, 4])) // ?
// mais ou menos argumentos
console.log(mmc(3)) // ?
console.log(mmc()) // ?
console.log(mmc(3, 4, 5)) // ?
console.log(mmc(3, 4, 5, 6)) // ?
// imagine outros casos especiais e teste de acordo
```

Faça o mesmo processo para o MDC.

---

Trick question (opcional), é possível fazer o seguinte funcionar?

```js
const numeros = [3, 4, 5]
console.log(numeros.mmc()) // 60
```

Se sim, go for it.