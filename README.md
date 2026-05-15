# Musk-mod-0
Prueba
const readline = require("readline-sync");

function crearMatriz(n) {
    const matriz = [];
    let contador = 1;
    for (let i = 0; i < n; i++) {
        const fila = [];
        for (let j = 0; j < n; j++) {
            fila.push(contador);
            contador++;
        }
        matriz.push(fila);
    }
    return matriz;
}

function imprimirFormatoBonito(matriz) {
    // Imprimir la primera fila con padding
    console.log("[ " + matriz[0].map(num => num.toString().padStart(3)).join(", ") + " ]");

    // Imprimir las filas siguientes
    for (let i = 1; i < matriz.length; i++) {
        // Al imprimir, aplicamos el mismo padding a cada número de la fila
        console.log(" " + matriz[i].map(num => num.toString().padStart(3)).join(", ") + " ");
    }
}

const n = parseInt(readline.question("Introduce el tamaño de la matriz cuadrada: "));

if (isNaN(n) || n <= 0) {
    console.log("Introduce un número entero mayor que 0.");
} else {
    const matriz = crearMatriz(n);
    imprimirFormatoBonito(matriz);

}

## dar formato de impresion a numeros grandes
