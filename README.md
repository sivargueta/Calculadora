# Calculadora
import math

def suma(a, b):
    return a + b
    
def resta(a, b):
    return a - b
    
def multiplicacion(a, b):
    return a * b
    
def division(a, b):
    return a / b if b != 0 else "Error: Division no se puede dividir por cero."
    
def potencia(a, b):
    return math.pow(a, b)
 
def modulo(a, b):
    return a % b if b != 0 else "Error: no se puede calcular modulo con divisor cero."

def main():
    while True:
        print("\nCalculadora")
        print("1. Suma")
        print("2. Resta")
        print("3. Multiplicacion")
        print("4. Division")
        print("5. Potencia")
        print("6. Modulo")
        print("0. Salir")
        
        try:
            opcion = int(input("Elija una operacion: "))
        except ValueError:
            print("Entrada no valida. Por favor, ingresa un numero.")
            continue
        
        if opcion == 0:
            print("Saliendo del programa...")
            break 

        if opcion < 1 or opcion > 6:
            print("Opcion no valida, intenta otra vez.")
            continue 
        
        try:
            num1 = float(input("Ingresa el primer numero: "))
            num2 = float(input("Ingresa el segundo numero: "))
        except ValueError:
            print("Entrada no valida. Por favor, ingresa un numero. ")
            continue
          
        if opcion == 1:
            resultado = suma(num1, num2)
            print(f"Suma: {num1}  +  {num2}  =  {resultado}")
        elif opcion == 2:
            resultado = resta(num1, num2)
            print (f"Resta: {num1} - {num2} = {resultado}")
        elif opcion == 3:
            resultado = multiplicacion(num1, num2)
            print(f"Multiplicacion: {num1} * {num2} = {resultado}")
        elif opcion == 4:
            resultado = division(num1, num2)
            print(f"Division: {num1} / {num2} = {resultado}")
        elif opcion == 5:
            resultado = potencia(num1, num2)
            print(f"Potencia:, {num1} ^ {num2} = {resultado}")
        elif opcion == 6:
            resultado = modulo(num1, num2)
            print(f"Modulo:, {int(num1)} % {int(num2)} = {resultado}")
            
            
        input("Presiona ENTER para continuar...")
      
if __name__ == "__main__":
    main()
