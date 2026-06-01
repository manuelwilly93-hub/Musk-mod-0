# Musk-mod-0
Prueba

``const readline = require("readline-sync");

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
console.log("[ [ " + matriz[0].join(", ") + " ],");

for (let i = 1; i < matriz.length - 1; i++) {
    console.log("  [ " + matriz[i].join(", ") + " ],");
  }
  console.log("  [ " + matriz[matriz.length - 1].join(", ") + " ] ]");
}
const n = parseInt(readline.question("Introduce el tamaño de la matriz cuadrada: "));

if (isNaN(n) || n <= 0) {
    console.log("Introduce un número entero mayor que 0.");
} else {
    const matriz = crearMatriz(n);
    imprimirFormatoBonito(matriz);

}``
