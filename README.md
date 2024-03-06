# target-processo-seletivo-2024
 
**1) Valor da variável SOMA:**

O valor da variável SOMA ao final do processamento será 91.

**2) Programa Sequência de Fibonacci:**

```dart
// o uso de iteração ao inves de recursividade para este caso é mais performatico
import 'package:test/test.dart';

bool pertenceSequenciaFibonacci(int numero) {
  int a = 0, b = 1;

  while (b < numero) {
    int temp = a;
    a = b;
    b = temp + b;
  }

  return b == numero;
}

void main() {
  test('Verifica se o número pertence à sequência de Fibonacci', () {
    expect(pertenceSequenciaFibonacci(13), isTrue);
    expect(pertenceSequenciaFibonacci(5), isTrue);
    expect(pertenceSequenciaFibonacci(8), isTrue);
    expect(pertenceSequenciaFibonacci(15), isFalse);
  });
}

```

**3) Próximos Elementos:**

a) 9

b) 128

c) 49

d) 100

e) 13

f) 20

**4) Descobrindo os Interruptores e Lâmpadas:**

1. Ligue o primeiro interruptor e aguarde alguns minutos.
2. Desligue o primeiro interruptor e ligue o segundo interruptor.
3. Entre na sala e veja as lâmpadas.
   - A lâmpada acesa está conectada ao segundo interruptor.
   - A lâmpada apagada e fria está conectada ao primeiro interruptor.
   - A lâmpada apagada e quente está conectada ao terceiro interruptor.

**5) Programa para Inverter uma String:**

```dart
// cuidado com o uso desta funcao para string grande , pois pode da string overflow, deve-se usar um string buffer.
String inverterString(String texto) {
  String stringInvertida = "";
  for (int i = texto.length - 1; i >= 0; i--) {
    stringInvertida += texto[i];
  }
  return stringInvertida;
}

void main() {
  String stringOriginal = "Hello";
  String stringInvertida = inverterString(stringOriginal);

  print("A string original: $stringOriginal");
  print("A string invertida: $stringInvertida");

  // Teste unitário
  test('Inverte a string corretamente', () {
    expect(inverterString('Hello'), equals('olleH'));
    expect(inverterString('12345'), equals('54321'));
    expect(inverterString('abcde'), equals('edcba'));
  });
}

```
