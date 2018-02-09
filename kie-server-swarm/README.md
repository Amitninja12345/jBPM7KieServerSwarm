# jBPM7KieServerSwarm

We can build the project with following profiles:

    BRM - includes BRM capability of the KIE Server that allows rules execution only
        no server components besides REST is configured
        build it with - mvn clean package -PBRM
    BPM - includes both BRM and BPM capabilities of the KIE Server - this is the default profile
        configures Swarm to have transactions and data sources enabled
        build it with - mvn clean package -PBPM or mvn clean package

Once build is finished start kie-server swarm using below command:

 java -Dorg.kie.server.id=swarm-kie-server -Dorg.kie.server.location=http://localhost:8380/server -jar target/kie-server-swarm-1.0-swarm.jar  com.example.swarm:DemoProject:1.0.1
