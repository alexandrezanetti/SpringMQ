# SpringMQ

# Site Source

https://developer.ibm.com/technologies/java/tutorials/mq-jms-application-development-with-spring-boot/

=====================================
# Montando o ambiente (estação de trabalho)
=====================================

# O projeto sample está no Git:

 https://github.com/alexandrezanetti/SpringMQ

 Obs.: já te coloquei no projeto

# Para usá-lo, basta fazer o clone:

  git clone https://github.com/alexandrezanetti/SpringMQ.git

# Se precisar, faça as alterações e comit no GIT usando os comandos abaixo:

 git add .

 git commit -ma

 git push 

# Para compilar o Java e gerar o Jar:

   mvn clean install

   Obs.: o jar ficará salvo no diretorio \target...

# Para colocar a app no ar (deixar rodando, pronta para chamadas):

   #ABRIR OUTRA CONSOLE e executar o comando abaixo:

   java -jar .\target\SpringMQ-0.0.1-SNAPSHOT.jar


# Os códigos de gravaçãoo e leitura estão no arquivo

    ZzzmqSpringBoot

      @GetMapping("MQCloud/Put")

      @GetMapping("MQCloud/Get")

=====================================
# Testando conexão com MQ Cloud
=====================================

Para conectar no meu MQ Cloud:

  set MQSERVER=CLOUD.ADMIN.SVRCONN/TCP/zzzqm-510a.qm.us-south.mq.appdomain.cloud(30907)
  
  runmqsc -c -u alexandre -w 60 ZZZQM

  Pass (apiKey): o1pVkgFCf7DxiDjQDlZZdAej4f6fPwWszCOJ0Zb5ZI20 

  E administrar como um Mq local:

   display qlocal(*) 

   ...

=====================================
# Gravando e lendo mensagens do MQCloud
=====================================

Para usar:

   Abrir um NOVO console (CMD) para PUT: 

     curl localhost:9200/MQCloud/Put


    Abrir um NOVO console (CMD) para GET: 

     curl localhost:9200/MQCloud/Get


   ATENCAO! Olhar a console para ver o Put e Get

