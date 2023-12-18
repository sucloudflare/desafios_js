# desafios_js

Readme para a Função aVeryBigSum
Visão Geral

Uma função em JavaScript, aVeryBigSum, foi criada para calcular a soma de um array de números inteiros grandes. Essa função foi projetada para lidar com casos em que inteiros regulares podem não ser suficientes devido ao seu tamanho.
Uso
Assinatura da Função

javascript


Calcula a soma de um array de números inteiros grandes.
 
@param {Array<Number>} ar - O array de inteiros a ser somado.
@returns {Number} - A soma dos elementos do array como um número regular.

function aVeryBigSum(ar) {
    // Implementação do código conforme descrito no Readme.
}

Parâmetros

    ar: Um array de inteiros que precisa ser somado.

Valor de Retorno

    A soma dos elementos do array como um número regular.

Detalhes de Implementação

A função usa um BigInt para lidar com possíveis problemas de estouro ao lidar com números inteiros grandes. Ela itera pelo array usando um loop for, convertendo cada elemento para um BigInt e adicionando-o à soma. O resultado final é opcionalmente retornado como um número regular.

javascript

```
    let sum = BigInt(0);

    for (let i = 0; i < ar.length; i++) {
    sum += BigInt(ar[i]);
    }

    return Number(sum);
```

Exemplo:


```
    const arrayDeNumeros = [1000000001, 1000000002, 1000000003, 1000000004, 1000000005];
    const resultado = aVeryBigSum(arrayDeNumeros);
    console.log(resultado); // Saída: 5000000015
```

Observação Importante

O uso de BigInt é crucial para evitar possíveis problemas de estouro ao lidar com números grandes. Se o resultado precisar ser usado como um número regular, a função Number() pode ser aplicada ao resultado do BigInt.
