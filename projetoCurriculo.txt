def form():
    file = open("index.html", "w")
    file.write("<body style='background-color: pink;'>\n")
    file.write("<h1 style='font-family: Candara;display:flex;align-items:center;justify-content:center; color: white;margin-top: 50px;'><b>CURRICULUM VITAE:</b></h1>\n")
    file.write("<div style='display:flex;align-items:left;justify-content:left;margin-right:auto;margin-left: auto;margin-top: 80px;width: 50%;border-radius: 5px;border-style: double;background-color:#C0D9D9';>\n")
    file.write("<div style='display: flex;justify-content: center;flex-direction: column;align-items: flex-start;padding-left: 80px;'>\n")

    def infos():
        nome = input("Digite seu nome: \n")
        idade = input("Digite sua idade: \n")
        endereco = input("Digite seu endereço: \n")
        telefone = input("Digite seu telefone para contato: \n")
        email = input("Digite seu email: \n")
        estCivil = input("Digite seu estado civil: \n")
        foto = input("Foto: (insira o link da foto desejada)\n")

        file.write("<div style='display:flex;flex-direction: row;align-items:center;justify-content:center;'>")
        file.write("<img style='width: 200px; height: 200px; margin-top: 50px;border-radius: 10px;' src='"+foto+"'>\n")
        file.write("<h1 style='font-family: Candara;padding-left: 100px;'>" + nome + "</h1><br>\n")
        file.write("</div><br>\n")

        file.write("<div style='font-size: 18px;'><b>Idade: </b>" + idade + " anos</div><br>")
        file.write("<div style='font-size: 18px;'><b>Endereço: </b>" + endereco + "</div><br>")
        file.write("<div style='font-size: 18px;'><b>Telefone: </b>" + telefone + "</div><br>")
        file.write("<div style='font-size: 18px;'><b>Email: </b>" + email + "</div><br>")
        file.write("<div style='font-size: 18px;'><b>Estado Civil: </b>" + estCivil + "</div><br>")
        file.write("<h2 style='align-items:center'>......................................................................................</h2>\n")

    def historico():
        continuar = 1
        file.write("<h2 style='font-family: Candara';>Experiencias Profissionais:</h2>\n")
        while continuar!= 2:
            experiencia = input("Digite suas experiencias passadas: \n")
            inicio = input("Digite data de inicio: \n")
            fim = input("Digite data do fim: \n")
            file.write("<li style= 'list-style: none;'><div style='font-size: 18px'><b>"+experiencia+"</b> de "+inicio+" à "+fim+"</div><br>")
            file.write("</li>")
            continuar = int(input("Digite 1 para adicionar mais experiencias ou 2 para sair: \n"))
        file.write("<h2 style='align-items:center'>......................................................................................</h2>\n")

    def idiomas():
        continuar = 1
        file.write("<h2 style='font-family: Candara';>Idiomas:</h2>\n")
        while continuar!= 2:
            lingua = input("Digite a linguagem do seu conhecimento: \n")
            nivel = input("Digite o nivel do conhecimento: \n")
            file.write("<li style= 'list-style: none;'><div style='font-size: 18px'><b>"+lingua+"</b> no nivel: "+nivel+"</div><br>")
            file.write("</li>")
            continuar = int(input("Digite 1 para adicionar mais experiencias ou 2 para sair: \n"))
        file.write("<h2 style='align-items:center'>......................................................................................</h2>\n")

    infos()
    historico()
    idiomas()
    file.write("</div>\n")
    file.write("</div>\n")
    file.write("</body>")
    file.close()
form()