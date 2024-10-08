## Challenge-03

### Scenario
* Similar scenario like challenge-01 (You are given a requirement to enhance a service)
* However, you will start seeing benefits of DevSpaces (Extensions + Tooling)

### Set Up + verification
* After DevSpaces initialization, check the extensions. You will see under "DevSpaces.apps.cluster" the extension "Language Support for Java(TM) by Red Hat" is already installed. This is done via the ".vscode/extensions.json" file
* Tools that are requires for development are already present : Type "oc --help", "jq --help" etc... This is possible because of the ds-challenge-02/devfile.yaml "tools" container (line#07)
* With tools and the extensions already part of the source code, your job becomes much easier to just start coding
* Open a terminal. Run the quarkus application in live coding mode with the command : "./mvnw quarkus:dev"
* Select your option "y/n" to the question (if asked) : Do you agree to contribute anonymous build time data to the Quarkus community? 
* Open another terminal and invoke "curl localhost:8080/api/greet/bengaluru". You will see empty result
* Openthe "src/main/java/org/acme/GreetingResource.java". You will observe the method "greetUser" needs to be fixed.

### Success Criteria
* Method "greetUser" is updated to accept a string as a parameter and returns a concatenated string of "Hello " and the passed name
* Invoking "curl localhost:8080/api/greet/bengaluru" will return "Hello bengaluru"
* Invoking "curl localhost:8080/api/greet/delta" will return "Hello delta"

### Resources
* https://quarkus.io/
* https://quarkus.io/guides/rest
* https://registry.devfile.io/viewer/devfiles/community/udi

### What did we learn
* Developers life is getting easier with required extensions already integrated via the DevSpaces. This takes the guess work out
* Developers do not have to worry about command line tools
* Taking one step forward to creating the developer joy. In this excercise, the developer still has to figure out how to compile, package etc.. Let's see how to address those in the next challenges

