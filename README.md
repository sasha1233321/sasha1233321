# Простой калькулятор

# Функция для сложения
def add(x, y):
    return x + y

# Функция для вычитания
def subtract(x, y):
    return x - y

# Функция для умножения
def multiply(x, y):
    return x * y

# Функция для деления
def divide(x, y):
    if y == 0:
        return "Ошибка: деление на ноль"
    return x / y

# Главная функция калькулятора
def calculator():
    while True:
        # Выводим меню
        print("Выберите операцию:")
        print("1. Сложение")
        print("2. Вычитание")
        print("3. Умножение")
        print("4. Деление")
        print("5. Выйти")

        choice = input("Введите номер операции (1/2/3/4/5): ")

        if choice == '5':
            print("Выход из калькулятора.")
            break

        if choice not in ('1', '2', '3', '4'):
            print("Некорректный ввод. Пожалуйста, выберите операцию из списка.")
            continue

        num1 = float(input("Введите первое число: "))
        num2 = float(input("Введите второе число: "))

        if choice == '1':
            print("Результат:", add(num1, num2))

        elif choice == '2':
            print("Результат:", subtract(num1, num2))

        elif choice == '3':
            print("Результат:", multiply(num1, num2))

        elif choice == '4':
            print("Результат:", divide(num1, num2))

        else:
            print("Некорректный ввод. Пожалуйста, выберите операцию из списка.")

# Запуск калькулятора
calculator()
