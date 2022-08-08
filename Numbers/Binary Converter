# Yo

def binary_to_decimal(x: str) -> float:
    if "." in x:
        x = x.split(".")
        x1 = x[0]
        result, n = 0, len(x1)-1
        for i in x1:
            if i == "1":
                result += 2 ** n
            n -= 1
        x2 = x[1]
        result1, n = 0, 1
        for i in x2:
            if i == "1":
                result += 1 / (2 ** n)
            n += 1
        final_result = result1 + result
        return final_result
    else:
        result, n = 0, len(x)-1
        for i in x:
            if i == "1":
                result += 2 ** n
            n -= 1
        return result


def decimal_to_binary(x: str) -> float:
    if "." in x:
        x = x.split(".")
        x1 = "{:b}".format(int(x[0]))

        x2 = float(f"0.{x[1]}")
        n = 0
        result = "."
        while n != 20:
            if not x2:
                return float(f"{x1}{result}")
            if x2*2*10 > 9:
                result += "1"
                x2 = round(x2*2-1, 2)
            else:
                x2 = x2 * 2
                result += "0"
            n += 1

        return float(f"{x1}{result}")

    else:
        x = "{:b}".format(int(x))
        return float(x)


def inputs():
    choice_input = input("Do you want to convert Decimal To Binary(1) or Binary To Decimal(2), enter 1 or 2: ")
    number_input = input("Enter a number: ")

    if choice_input == "1" and number_input.isnumeric():
        print(decimal_to_binary(number_input))
    elif choice_input == "2" and number_input.isnumeric():
        print(binary_to_decimal(number_input))
    else:
        raise ValueError


print("\nHi, this program converts binary numbers to decimal and visa versa")

while True:
    inputs()
    try_again = input("Try again? y/n: ")
    if try_again == "y":
        continue
    else:
        exit()
