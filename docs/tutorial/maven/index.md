# Como instalar o Maven? 

## Passo 1 - Verifique a instalação do Java

Verifique que a variável de ambiente JAVA_HOME esteja configurada corretamente. 

**Windows**

Você pode verificar a instalação executando o comando abaixo:

    echo %JAVA_HOME%

**Linux**

Você pode verificar a instalação executando o comando abaixo:

    echo $JAVA_HOME


A saída deve ser igual ao caminho onde você decidiu instalar o Java.

## Passo 2 - Faça o download do Maven

**Windows**

https://www-eu.apache.org/dist/maven/maven-3/3.6.0/binaries/apache-maven-3.6.0-bin.zip

**Linux**

https://www-eu.apache.org/dist/maven/maven-3/3.6.0/binaries/apache-maven-3.6.0-bin.tar.gz

## Passo 3 - Extraia o arquivo em um diretório da sua escolha

**Windows**

    unzip apache-maven-3.6.0-bin.zip

**Linux**

    tar xzvf apache-maven-3.6.0-bin.tar.gz

## Passo 4 - Adicione o maven no PATH

Adicione o diretório bin que está dentro do diretório do maven à variável de ambieente PATH.

**Windows**

No prompt de comando execute o seguinte comando:

    setx PATH %PATH%;<caminho_para_o_maven>\bin

Feche o Prompt.

**Linux**

No terminal execute o seguinte comando:

    sudo gedit /etc/profile

Adicione as linhas abaixo no início do arquivo /etc/profile

PATH=$PATH:<caminho_para_o_maven>/bin
export PATH


Salve o arquivo e reinicie a sua máquina para que as modificações sejam aplicadas.

## Passo 5 - Faça um teste

Para testar que a configuração está funcionando, você pode executar o comando abaixo no terminal ou no promt de comando.

    mvn -v

O resultado deve parecer com a saída a seguir.

    Apache Maven 3.6.0 (97c98ec64a1fdfee7767ce5ffb20918da4f719f3; 2018-10-24T20:41:47+02:00)
    Maven home: /opt/apache-maven-3.6.0
    Java version: 1.8.0_45, vendor: Oracle Corporation
    Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_45.jdk/Contents/Home/jre
    Default locale: en_US, platform encoding: UTF-8
    OS name: "mac os x", version: "10.8.5", arch: "x86_64", family: "mac"

