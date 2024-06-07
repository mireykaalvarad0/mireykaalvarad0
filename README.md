## Hi there 👋

- 🔭 I’m currently working on Cineplanet.
- 🌱 I’m currently learning React.
- 👯 I’m looking to collaborate on rpojects.
- 🤔 I’m looking for help with Next.js.
- 💬 Ask me about my favorites programing language.
- 📫 How to reach me: mireykaalvarad0.
- 😄 Pronouns: mireyka.
- ⚡ Fun fact: I paid for WinRAR.

<!DOCTYPE html>
<html>
<head>
  <title>Ejemplo de JavaScript</title>
  <meta charset="UTF-8">
</head>
<body>

<div id="contenido"></div>

<script>
  // Esperar a que el DOM se haya cargado completamente
  document.addEventListener('DOMContentLoaded', function() {
    // Obtener el elemento por su id
    var contenido = document.getElementById('contenido');
    
    // Insertar contenido HTML
    contenido.innerHTML = 'Andrea Alvarado<br>44';
  });
</script>

</body>
</html>

<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="contenido"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let nombre = 'Juan';
            let edad = 10;
            let altura = 1.92;
            let casado = false;

            let contenido = document.getElementById('contenido');
            contenido.innerHTML = `
                <p>Nombre: ${nombre}</p>
                <p>Edad: ${edad}</p>
                <p>Altura: ${altura}</p>
                <p>Casado: ${casado}</p>
            `;
        });
    </script>

</body>

</html>



<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="mensaje"></div>

    <script>
        // Función para obtener y mostrar los datos del usuario
        function obtenerDatosUsuario() {
            let nombre = prompt('Ingrese su nombre:');
            let edad = prompt('Ingrese su edad:');

            // Validar las entradas del usuario
            if (nombre && edad) {
                // Crear el mensaje
                let mensaje = `Hola ${nombre}, así que tienes ${edad} años.`;

                // Obtener el elemento div y actualizar su contenido
                let mensajeDiv = document.getElementById('mensaje');
                mensajeDiv.textContent = mensaje;
            } else {
                alert('Por favor ingrese tanto su nombre como su edad.');
            }
        }

        // Esperar a que el DOM se cargue antes de ejecutar el script
        document.addEventListener('DOMContentLoaded', obtenerDatosUsuario);
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            let valor1 = prompt('Ingrese primer número:');
            let valor2 = prompt('Ingrese segundo número:');

            // Validar entradas
            if (isNaN(valor1) || isNaN(valor2) || valor1 === '' || valor2 === '') {
                alert('Por favor ingrese valores numéricos válidos.');
            } else {
                // Convertir a números
                valor1 = parseFloat(valor1);
                valor2 = parseFloat(valor2);

                // Calcular suma y producto
                let suma = valor1 + valor2;
                let producto = valor1 * valor2;

                // Mostrar resultados
                let resultadoDiv = document.getElementById('resultado');
                resultadoDiv.innerHTML = `
                    <p>La suma es: ${suma}</p>
                    <p>El producto es: ${producto}</p>
                `;
            }
        });
    </script>

</body>

</html>




<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let nombre = prompt('Ingrese nombre:');
            let nota = parseInt(prompt('Ingrese su nota:'));

            // Validar que la nota sea un número
            if (isNaN(nota)) {
                alert('Por favor ingrese un número válido para la nota.');
            } else {
                let resultadoDiv = document.getElementById('resultado');
                if (nota >= 4) {
                    resultadoDiv.textContent = `${nombre} está aprobado con un ${nota}.`;
                } else {
                    resultadoDiv.textContent = `${nombre} no está aprobado. Su nota es ${nota}.`;
                }
            }
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>
    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            let num1 = prompt('Ingrese el primer número:');
            let num2 = prompt('Ingrese el segundo número:');
            // Validar que las entradas sean números
            if (isNaN(num1) || isNaN(num2) || num1 === '' || num2 === '') {
                alert('Por favor, ingrese valores numéricos válidos.');
            } else {
                num1 = parseFloat(num1);
                num2 = parseFloat(num2);
                let resultadoDiv = document.getElementById('resultado');
                if (num1 > num2) {
                    resultadoDiv.textContent = 'El mayor es ' + num1;
                } else if (num2 > num1) {
                    resultadoDiv.textContent = 'El mayor es ' + num2;
                } else {
                    resultadoDiv.textContent = 'Ambos números son iguales.';
                }
            }
        });

    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let nota1 = prompt('Ingrese 1ra. nota:');
            let nota2 = prompt('Ingrese 2da. nota:');
            let nota3 = prompt('Ingrese 3ra. nota:');

            // Validar que las entradas sean números
            if (isNaN(nota1) || isNaN(nota2) || isNaN(nota3) || nota1 === '' || nota2 === '' || nota3 === '') {
                alert('Por favor, ingrese valores numéricos válidos.');
                return;
            }

            // Convertir las entradas a números
            nota1 = parseFloat(nota1);
            nota2 = parseFloat(nota2);
            nota3 = parseFloat(nota3);

            // Calcular el promedio
            let promedio = (nota1 + nota2 + nota3) / 3;

            // Determinar el resultado
            let resultado;
            if (promedio >= 7) {
                resultado = 'promocionado';
            } else if (promedio >= 4) {
                resultado = 'regular';
            } else {
                resultado = 'reprobado';
            }

            // Mostrar el resultado en el DOM
            let resultadoDiv = document.getElementById('resultado');
            resultadoDiv.textContent = `El promedio es ${promedio.toFixed(2)}. Estás ${resultado}.`;
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let num1 = prompt('Ingrese el primer número:');
            let num2 = prompt('Ingrese el segundo número:');
            let num3 = prompt('Ingrese el tercer número:');

            // Validar que las entradas sean números
            if (isNaN(num1) || isNaN(num2) || isNaN(num3) || num1 === '' || num2 === '' || num3 === '') {
                alert('Por favor, ingrese valores numéricos válidos.');
                return;
            }

            // Convertir las entradas a números
            num1 = parseFloat(num1);
            num2 = parseFloat(num2);
            num3 = parseFloat(num3);

            // Determinar el mayor número
            let mayor;
            if (num1 >= num2 && num1 >= num3) {
                mayor = num1;
            } else if (num2 >= num3) {
                mayor = num2;
            } else {
                mayor = num3;
            }

            // Mostrar el resultado en el DOM
            let resultadoDiv = document.getElementById('resultado');
            resultadoDiv.textContent = `El mayor es el ${mayor}.`;
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let dia = prompt('Ingrese día:');
            let mes = prompt('Ingrese mes:');
            let año = prompt('Ingrese año:');

            // Validar que las entradas sean números
            if (isNaN(dia) || isNaN(mes) || isNaN(año) || dia === '' || mes === '' || año === '') {
                alert('Por favor, ingrese valores numéricos válidos.');
                return;
            }

            // Convertir las entradas a números
            dia = parseInt(dia);
            mes = parseInt(mes);
            año = parseInt(año);

            // Validar la fecha (básica)
            if (dia < 1 || dia > 31 || mes < 1 || mes > 12 || año < 1) {
                alert('Por favor, ingrese una fecha válida.');
                return;
            }

            // Determinar si el mes corresponde al primer trimestre
            let resultadoDiv = document.getElementById('resultado');
            if (mes == 1 || mes == 2 || mes == 3) {
                resultadoDiv.textContent = 'Corresponde al primer trimestre del año.';
            } else {
                resultadoDiv.textContent = 'No corresponde al primer trimestre del año.';
            }
        });
    </script>

</body>

</html>



<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let valor = prompt('Ingrese un valor comprendido entre 1 y 5:');

            // Validar que la entrada sea un número
            if (isNaN(valor) || valor === '') {
                alert('Por favor, ingrese un valor numérico válido.');
                return;
            }

            // Convertir la entrada a número entero
            valor = parseInt(valor);

            // Validar que el número esté en el rango adecuado
            if (valor < 1 || valor > 5) {
                alert('Por favor, ingrese un valor comprendido entre 1 y 5.');
                return;
            }

            // Determinar el valor en palabras usando switch
            let resultado;
            switch (valor) {
                case 1:
                    resultado = 'uno';
                    break;
                case 2:
                    resultado = 'dos';
                    break;
                case 3:
                    resultado = 'tres';
                    break;
                case 4:
                    resultado = 'cuatro';
                    break;
                case 5:
                    resultado = 'cinco';
                    break;
            }

            // Mostrar el resultado en el DOM
            let resultadoDiv = document.getElementById('resultado');
            resultadoDiv.textContent = resultado;
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let resultadoDiv = document.getElementById('resultado');
            let fragment = document.createDocumentFragment();

            for (let x = 1; x <= 100; x++) {
                let p = document.createElement('p');
                p.textContent = x;
                fragment.appendChild(p);
            }

            resultadoDiv.appendChild(fragment);
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let suma = 0;
            let valor;
            
            for (let x = 1; x <= 5; x++) {
                valor = prompt(`Ingrese valor ${x}:`);

                // Validar que la entrada sea un número
                if (isNaN(valor) || valor === '') {
                    alert('Por favor, ingrese un valor numérico válido.');
                    x--; // Reducir el contador para repetir esta iteración
                    continue;
                }

                // Convertir la entrada a número entero y sumar
                suma += parseInt(valor);
            }

            // Mostrar el resultado en el DOM
            let resultadoDiv = document.getElementById('resultado');
            resultadoDiv.textContent = `La suma de los valores es ${suma}.`;
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let valor;
            let resultadoDiv = document.getElementById('resultado');

            do {
                valor = prompt('Ingrese un valor entre 0 y 999:');
                
                // Validar que la entrada sea un número dentro del rango
                if (isNaN(valor) || valor === '' || valor < 0 || valor > 999) {
                    alert('Por favor, ingrese un valor numérico válido entre 0 y 999.');
                    continue;
                }

                // Convertir la entrada a número entero
                valor = parseInt(valor);

                // Determinar la cantidad de dígitos
                let digitos;
                if (valor < 10) {
                    digitos = '1 dígito';
                } else if (valor < 100) {
                    digitos = '2 dígitos';
                } else {
                    digitos = '3 dígitos';
                }

                // Mostrar el resultado en el DOM
                let p = document.createElement('p');
                p.textContent = `El valor ${valor} tiene ${digitos}.`;
                resultadoDiv.appendChild(p);

            } while (valor != 0);
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            let resultadoDiv = document.getElementById('resultado');
            let numeros = '';
            
            for (let f = 1; f <= 10; f++) {
                numeros += f + ' ';
            }
            
            // Mostrar el resultado en el DOM
            resultadoDiv.textContent = numeros;
        });
    </script>

</body>

</html>


<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="mensaje"></div>

    <script>
        function mostrarMensaje() {
            let mensajeDiv = document.getElementById('mensaje');
            let mensaje = "Cuidado<br>Ingrese su documento correctamente<br>";
            mensajeDiv.innerHTML += mensaje;
        }

        mostrarMensaje();
        mostrarMensaje();
        mostrarMensaje();
    </script>

</body>

</html>



<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <div id="resultado"></div>

    <script>
        function mostrarComprendidos(inicio, fin) {
            let resultadoDiv = document.getElementById('resultado');
            let numeros = '';
            for (let f = inicio; f <= fin; f++) {
                numeros += f + ' ';
            }
            resultadoDiv.textContent = numeros;
        }

        let valor1 = parseInt(prompt('Ingrese valor inferior:'));
        let valor2 = parseInt(prompt('Ingrese valor superior:'));
        mostrarComprendidos(valor1, valor2);
    </script>

</body>

</html>



<!DOCTYPE html>
<html>

<head>
    <title>Ejemplo de JavaScript</title>
    <meta charset="UTF-8">
</head>

<body>

    <script>
        function formatearFecha(dia, mes, año) {
            const nombresMeses = [
                'enero', 'febrero', 'marzo', 'abril', 'mayo', 'junio',
                'julio', 'agosto', 'septiembre', 'octubre', 'noviembre', 'diciembre'
            ];

            if (mes < 1 || mes > 12) {
                return 'Mes inválido';
            }

            return `Hoy es ${dia} de ${nombresMeses[mes - 1]} de ${año}`;
        }

        document.write(formatearFecha(27, 1, 2021));
    </script>

</body>

</html>