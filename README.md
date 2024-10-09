## Challenge-03

### Scenario
* Lets continue to enhance the ds-challenge-02
* So far we have done consistent way of creating tooling and extensions. Let's take a step further by enhancing this to create consistent way to build, package, run the programs and also creating standardized end points

### Set Up + verification
* Reminder : You should have created this workspace from your teams challenges folder in source control
* It's time to create standardized commands. You will create two commands in devfile.yaml
    * Create 1st command with id "1-package" and label (1. Package the application) inside devfile to execute "mvn package"
    * Create 2nd command with id "2-startdev" and lable (2. Start Development mode) inside devfile to execute "mvw compile quarkus:dev"
    * Leverage the Resources section and find how you can create commands in devfile.yaml
* Creating Two Endpoints
    * The "src/main/java/org/acme/GreetingResource.java" has restful endpoints : 
        * localhost:8080
        * localhost:8080/api/hello
        * localhost:8080/api/greet/#input
    * Create 1st endpoint for "/api/hello" [with name="greet-attendee"]
    * Create 2nd endpoint for the root "/" [with name=base-challenge]
    * Leverage the Resources section and find how you can create endpoints in devfile.yaml    
* Once you complete the above, commit the changes back to the repository
* Open the repository in devspaces from your teams
* So, we have our extension "Language Support for Java(TM) by Red Hat" and tools that are required for development are already present : Type "oc --help", "jq --help" etc are already installed
* In devspaces, Open a terminal. Run the command "chmod 755 mvnw" to change the mvnw file to be executable
* Run the quarkus application using commands "2. Start Development mode" you created in devfile. See success criteria on how to run the command
* Select your option "y/n" to the question (if asked) : Do you agree to contribute anonymous build time data to the Quarkus community?
* If things don't look OK, delete the workspace, update the devfile directly in source control and recreate the workspace


### Success Criteria
* Commands are created and can be invoked via the "Hamburger Icon --> Terminal --> Run Task --> Devfile --> Select #Commands"
* Endpoints (shown in the bottom left corner of the IDE) can be invoked
* Invoking localhost:8080 displays an image of the "Developer Flow"
* Invoking localhost:8080/api/hello displays a response "Hello Challenge Attendees"

### Resources
* https://devfile.io/docs/2.2.2/adding-commands
* https://devfile.io/docs/2.2.2/defining-endpoints
* https://devfile.io/docs/2.2.2/devfile-schema

### What did we learn
* In addition to the extensions and tooling, now we have consitent endpoints and commands. This makes iterative development faster (no more typing commands and or finding endpoints via code)
* The next developer will know exactly how things are done making it a much better experience
* One of the core functions of development is to Test & Debug code. In the next challenge, we will explore debugging inside DevSpaces

