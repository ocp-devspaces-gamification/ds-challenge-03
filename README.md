## Challenge-03

### Scenario
* Lets continue to enhance the ds-challenge-02
* So far we have done consistent way of creating tooling and extensions. Let's take a step further by enhancing this to create consistent way to build, package, run the programs and also creating standardized end points

### Set Up + verification
* Ensure this workspace is created from your teams source control folder
* So, we have our extension "Language Support for Java(TM) by Red Hat" and tools that are required for development are already present : Type "oc --help", "jq --help" etc are already installed
* Open a terminal. Run the command "chmod 755 mvnw" to change the mvnw file to be executable
* It's time to create standardized commands. You will create two commands
    * Create 1st command with id "1-package" and label (1. Package the application) inside devfile to execute "mvn package"
    * Create 2nd command with id "2-startdev" and lable (2. Start Development mode) inside devfile to execute "mvw compile quarkus:dev"
    * Leverage the Resources section and find how you can create commands in devfile.yaml
    * To see changes, you will have to restart the workspace
* Creating Endpoints
    * The "src/main/java/org/acme/GreetingResource.java" has restful endpoints : 
        * localhost:8080
        * localhost:8080/api/hello
        * localhost:8080/api/greet/#input
    * Create endpoint for "/api/hello" [name="greet-attendee"]
    * Create endpoint for the root "/" [name=base-challenge]
    * Leverage the Resources section and find how you can create endpoints in devfile.yaml    
* Once you complete the above
    * commit the changes back to the repository
    * Delete the workspace created & recreate with the updated devfile
    * Run the quarkus application in live coding mode with commands you created in devfile
* Select your option "y/n" to the question (if asked) : Do you agree to contribute anonymous build time data to the Quarkus community?

### Success Criteria
* Commands are created and can be invoked via the "Hamburger Icon --> Terminal --> Run Task --> Devfile --> Select #Commands"
* Endpoints (shown in the bottom left corner of the IDE) can be invoked
* Invoking localhost:8080 displays an image of the "Developer Flow"
* Invoking localhost:8080/api/hello displays a response "Hello Challenge Attendees"

### Resources
* https://devfile.io/docs/2.2.2/adding-commands
* https://devfile.io/docs/2.1.0/defining-endpoints
* https://devfile.io/docs/2.1.0/devfile-schema

### What did we learn
* In addition to the extensions and tooling, now we have consitent endpoints and commands. This makes iterative development faster (no more typing commands and or finding endpoints via code)
* The next developer will know exactly how things are done making it a much better experience
* One of the core functions of development is to debug code. In the next challenge, we will explore debugging inside DevSpaces

