# Como instalar o Visual Studio Code no Linux manualmente

## Para instalar o Visual Studio Code no Linux manualmente, faça o seguinte:
Passo 1. Abra um terminal;
Passo 2. Caso já tenha feito alguma instalação manual, apague a pasta, o link e o atalho anterior com esse comando;

` sudo rm -Rf /opt/vscode/* `

` sudo rm -Rf /opt/vscode/code `

` sudo rm -Rf /usr/share/applications/vscode.desktop `

Passo 3. Confira se o seu sistema é de 32 bits ou 64 bits, para isso, use o seguinte comando no terminal:

` uname -m `

Passo 4. Se seu sistema é de 32 bits, use o comando abaixo para baixar o programa. Se o link estiver desatualizado, acesse essa página, baixe a última versão e salve-o com o nome vscode.tar.gz:

` wget "https://go.microsoft.com/fwlink/?LinkID=620885" -O vscode.tar.gz `

Passo 5. Se seu sistema é de 64 bits, use o comando abaixo para baixar o programa. Se o link estiver desatualizado, acesse essa página, baixe a última versão e salve-o com o nome vscode.tar.gz:

` wget "https://go.microsoft.com/fwlink/?LinkID=620884" -O vscode.tar.gz `

Passo 6. Use o comando a seguir para descompactar o arquivo baixado;

` sudo tar -vzxf vscode.tar.gz -C /opt/ `

Passo 7. Renomeie o arquivo criado, para deixar seu nome em letras minúsculas;

` sudo mv /opt/VSCode*/ /opt/vscode/ `

Passo 8. Finalmente, crie um atalho para facilitar a execução do programa;

` sudo ln -sf /opt/vscode/code /usr/bin/code `

Passo 9. Se seu ambiente gráfico atual suportar, crie um lançador para o programa, executando o comando abaixo;

` echo -e '[Desktop Entry]\n Version=1.0\n Name=vscode\n Exec=/opt/vscode/code\n Icon=/opt/vscode/resources/app/resources/linux/code.png\n Type=Application\n Categories=Application' | sudo tee /usr/share/applications/vscode.desktop `

Posteriormente, se for necessário, para remover o Visual Studio Code no Linux, basta apagar a pasta, o link e o atalho anterior com esse comando;

` sudo rm -Rf /opt/vscode/* `

` sudo rm -Rf /opt/vscode/code `

` sudo rm -Rf /usr/share/applications/vscode.desktop `

Fonte: [Blog do Edivaldo](http://www.edivaldobrito.com.br/visual-studio-code-no-linux/)
