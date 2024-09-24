EXERCICIO-1
#Calculadora de Logaritmo

    import math

    a = float(input("Digite o valor de a: "))
    b = float(input("Digite o valor de b: "))
    e = float(input("Digite o erro de precisao: "))

    log = math.log10(b - a)

    log_e = math.log10(e)

    log_2= math.log10(2)

    k = (log - log_e) / log_2

    print (k)

    print(" ")

    for i in range(round(k + 1)):

         xk = (a + b) / 2

        fa = ((5 - a ) ** (1/2)) - 2 ** (a-1)

        fx = ((5 - xk ) ** (1/2)) - 2 ** (xk-1)

        erro = b - a
        sinal = str()
        soma = (fa) * (fx)
        if soma < 0:
            print(f'{a:,.3f} | {b:,.3f} | {xk:,.3f} | {fa:,.3f} | {fx:,.3f}  |  - | {erro:,.3f}')
        if soma > 0:
            print(f'{a:,.3f} | {b:,.3f} | {xk:,.3f} | {fa:,.3f} | {fx:,.3f}  |  + | {erro:,.3f}')

    
        if soma < 0: 
            b = xk
        

        else:
            a = xk   

        if fx < e and fx > 0:
            valor = xk

    print (f"A resposta é : {valor}")



EXERCICIO-2
#Calculadora de Logaritmo

    import math

    a = float(input("Digite o valor de a: "))
    b = float(input("Digite o valor de b: "))
    e = float(input("Digite o erro de precisao: "))

    log = math.log10(b - a)


    log_e = math.log10(e)

    log_2= math.log10(2)

    k = (log - log_e) / log_2

    print(k)
    print(" ")

    for i in range(round(k + 1)):

        xk = (a + b) / 2

        fa = math.log(3*a - 1) + 2 * a

        fx = math.log(3*xk - 1) + 2 * xk

        erro = b - a
        soma = (fa) * (fx)
        if soma < 0:
            print(f'{a:,.2f} | {b:,.2f} | {xk:,.3f} | {fa:,.3f} | {fx:,.3f}  | - | {erro:,.3f}')
        if soma > 0:
            print(f'{a:,.2f} | {b:,.2f} | {xk:,.3f} | {fa:,.3f} | {fx:,.3f}  | + | {erro:,.3f}')
    
        if soma < 0: 
            b = xk
        

        else:
            a = xk   

    if fx < e and fx > 0:
        print(f"O valor obtido é: {xk:,.3f}")
