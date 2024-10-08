## Challenge-03

### Scenario
* Similar scenario like challenge-01 (You are given a requirement to enhance a service)
* However, you will start seeing benefits of DevSpaces (Extensions + Tooling)

### Set Up + verification
* After DevSpaces initialization, check the extensions. You will see under "DevSpaces.apps.cluster" the extension "Language Support for Java(TM) by Red Hat" is already installed. This is done via the ".vscode/extensions.json" file
* Tools that are requires for development are already present : Type "oc --help", "jq --help" etc... This is possible because of the ds-challenge-02/devfile.yaml "tools" container (line#07)
* With tools and the extensions already part of the source code, your job becomes much easier to just start coding
* Open a terminal. Run the command "chmod 755 mvnw" to change the mvnw file to be executable
* Run the quarkus application in live coding mode with the command : "./mvnw quarkus:dev"
* Select your option "y/n" to the question (if asked) : Do you agree to contribute anonymous build time data to the Quarkus community? 
* Open another terminal and invoke "curl localhost:8080/api/greet/bengaluru". You will see empty result
* Openthe "src/main/java/org/acme/GreetingResource.java". You will observe the method "greetUser" needs to be fixed.

### Success Criteria
* 
* 
* 

### Resources
* https://devfile.io/docs/2.1.0/defining-endpoints
* https://devfile.io/docs/2.1.0/devfile-schema

### What did we learn
* 
* 
* 

