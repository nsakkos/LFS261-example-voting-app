FROM maven:3.6.1-jdk-8-slim
WORKDIR /app
COPY . .
RUN --network=my-bridge-network mvn package && \
mv target/worker-jar-with-dependencies.jar /run/worker.jar && rm -rf /app/*
CMD java -jar /run/worker.jar
