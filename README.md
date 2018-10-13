# rabbitmq-java
ejecutar

./gradlew build shadowJar

export MQ_URL=${MQ_URL_DE_PIVOTAL}

 java -jar build/libs/rabbitmq-java-all.jar
 
 
 -- subir a pivotal
 cf push --no-start
 
 cf set-env rabbitmq-java MQ_URL ${MQ_URL_DE_PIVOTAL}
###Variable optenida de pivotal

cf rabbitmq-java --start