# Como instalar o Java?

## Passo 1. Entre no site da Oracle e faça o download

Faça o download do  Java SE Development Kit 8 no site da Oracle, de acordo com o seu sistema operacional.
Atente-se para baixar o pacote compactado com tar.gz caso seu sistema operacional seja Linux.

[Link para o site da Oracle](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)

## Passo 2. Execute o instalador

Após o download do arquivo de instalação ter sido concluído, a instalação do JDK é feita executando o programa de instalação.

### Para o Windows

Executar o programa de instalação e clicar nSxt em todas as telas apresentadas. O processo é simples e rápido.S

### Para o Linux

Abra um terminal, vá para a pasta Downloads e copie o arquivo de instalação para o diretório de sua preferência com o comando abaixo

`cp jdk-<versão>.tar.gz <caminho-completo-do-seu-diretório>`

Mude para o diretório que vc escolheu 

`cd /<caminho-completo-do-seu-diretório>`

Descompacte o arquivo com o comando a seguir

`tar -zvxf jdk-<versão>.tar.gz`

## Passo 3. Configurando o Java

A configuração consiste na criação das variáveis de ambiente JAVA_HOME e CLASSPATH. Estas variáveis são importantes para que os programas encontrem onde o JDK foi instalado.

### Para o Windows

Execute os comandos abaixo no prompt de comando
        
`setx JAVA_HOME "<diretório-onde-jdk-foi-instalado>"`

`setx CLASSPATH %JAVA_HOME%\lib`

`setx PATH %PATH%;%JAVA_HOME%\bin`
    
Feche o Prompt.

### Para o Linux

Abra o terminal e edite o arquivo /etc/profile como o comando abaixo    
    
`sudo gedit /etc/profile`
    
Adicione as linhas abaixo no início do arquivo /etc/profile
    
    JAVA_HOME=diretório-onde-jdk-foi-instalado
    CLASSPATH=.;$JAVA_HOME/lib
    PATH=$PATH:$JAVA_HOME/bin
    export JAVA_HOME
    export CLASSPATH
    export PATH
    
Salve o arquivo e reinicie a sua máquina para que as modificações sejam aplicadas. 

## Passo 4. Testando a configuração

Abrir o Terminal do Linux ou o prompt do Windows e execute o seguinte comando:
    
`java -version`

A saída do terminal deve ser algo parecido com a imagem abaixo, onde pode-se ler a versão do Java instalado.

![java version](http://2.bp.blogspot.com/-6nuMEHx_lWs/TqJtyZQcLvI/AAAAAAAAAeg/_KtSa2esueo/s1600/Java1.JPG)
