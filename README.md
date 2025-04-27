# java-tools-docs
--------------------------
      1) when we run any java application we can provide two types of arguments
         1) jvm arguments
         2) program arguments
        
      suppose you working with spring boot application , to run the application you will execute following command.
      java -jar app.jar
      
      what is thumb rule to provide above 2 types of arguments
      jvm arguments always put just after java command and program-args always just after artifacts name.
      
      Syntax:
       java <jvm-args> -jar app.jar <program-args>
      
      
       jvm arguments types
      ------------------------------------------------
      basically we have many types basically most frequently used type are 2.
      1) start with -D  [D="Define system property"]  --this is use to pass jvm./system properties like -Dnode.name=dev1
      2) start with -X  [X = "extended option"] -- this is use to provide configuration for jvm[like heap memory[intial,max], stack size]
      3) start with -XX:  [XX = "eXtended eXperimental options"] -- They are advanced JVM settings — deeper than -X options
      
         ms --heap initial size [k,m,g{kb,mb,gb}]   ms = memory start
         mx --heap max size   [k,m,g{kb,mb,gb}]   mx = memory max
         ss -- stack size  [k,m,g{kb,mb,gb}]   ss = stack size
         
      example  for max heap size 3 GB
      -----------------------------------------
      java -Xmx3g -jar app.jar  or java -X3072m -jar app.jar
      
      example for min 2 gb and max 3GB
      -----------------------------------
      java  -Xms2g -Xmx3g -jar app.jar  or java -Xms2048m -X3072m -jar app.jar
      
      example for min 2 gb and max 3GB and stack size of 100mb
      ----------------------------------------------------------
      java  -Xms2g -Xmx3g -Xss100m -jar app.jar  or java -Xms2048m -X3072m -Xss100m -jar app.jar
      
      example  for max heap size 3 GB and system node.name propery
      ----------------------------------------------------------------
      java -Xmx3g -jar -Dnode.name=dev1 app.jar  or java -X3072m -Dnode.name=dev1 -jar app.jar


      alomost all jvm flag can be set or print using following syntax.

      -XX:+FlagName  --for print like -XX:+PrintFlagsFinal
      -XX:FlagName=Value for setting value like - XX:HeapDumpOnOutOfMemoryError=true
      




