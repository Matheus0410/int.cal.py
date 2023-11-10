print("Bem vindo a calculadora\n")

#função de adição

def add(x, y):
    return x + y

#função de subtração
def subtract(x, y):
    return x - y

# função de multiplicar dois numeros
def multiply(x, y):
    return x * y

# função de divisão de dois numeros
def divide(x, y):
    return x / y


print("Selecione a operação.")
print("1.Adição")
print("2.Subtração")
print("3.Multiplicação")
print("4.Divisão")

while True:

    choice = input("escolha entre (1/2/3/4):\n")

    # o usuario deve escolher entre as quatro opções:
    if choice in ('1', '2', '3', '4'):
        try:
            num1 = float(input("Entre com o primeiro numero:\n "))
            num2 = float(input("Entre com o segundo numero:\n "))
        except ValueError:
            print("Entrada errada. Por favor digite um numero.\n")
            continue

        if choice == '1':
            print(num1, "+", num2, "=", add(num1, num2))

        elif choice == '2':
            print(num1, "-", num2, "=", subtract(num1, num2))

        elif choice == '3':
            print(num1, "*", num2, "=", multiply(num1, num2))

        elif choice == '4':
            print(num1, "/", num2, "=", divide(num1, num2))
        
      
        next_calculation = input("deseja fazer mais uma operação? (sim/nao):\n ")
        if next_calculation == "nao":
          break
    else:
        print("entrada incorreta")
