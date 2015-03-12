#Cucumber

- The default folder for features in cucumber is `features`
- __feature:__ Each Cucumber test is called a feature. Each feature contains steps which tells Cucumber what to do
- __Gherkin:__ It is the name of the syntax
- In order to check the syntax of a file we can use the following command
    cucumber features/test.feature --dry-run

#Keywords

##Feature
* It explains the summary of the test. It does not effect the behaviour of the test
* The text immediately following the "Feature" keyword is the name of the feature
* The remaining lines after the Feature keyword is the description. It cannot contain "Background", "Scenario Outline" or "Scenario"
* Description is the best place to  explain the feature and add the docs and user surveys
 
 ####Example
        Feature: This is the feature title
        
        This is the description of the feature, which can
        span multiple lines.
        You can even include empty lines, like this one:
        In fact, everything until the next Gherkin keyword is included  
        in the description.
* It’s conventional to name the feature file by converting the feature’s name to lowercase characters and replacing the spaces with underscores.
* Feature must be followed by either __Background__, __Scenario__ or __Scenario Outline__ in a valid Gherkin
* A good template for the *description*:
            
            In order to <meet some goal> 
            As a <type of stakeholder> 
            I want <a feature>

##Scenario
It is a single concrete example of how the system should behave under a specific situation.

* Each feature has typically 5-20 scenarios
* Steps in a scenario:
        
            Take system to a particular state ---> Poke it ---> Examine the new state

##Given, When, Then
* __Given:__ It sets the context of the scenario
*  __When:__ It is to interact somehow with the system
*  __Then:__ Checks the outcome of the interaction with expected behaviour

## And, But
We can add more steps to _Given_, _When_, _Then_
* _And_, _But_ do not make a difference to Cucumber. They are there to make the scenario more readable

## Bullets
It can be used to replace _Given_,_When_,_Then_
* It reduces the readability of the scenario a bit
#Cucumber

- The default folder for features in cucumber is `features`
- __feature:__ Each Cucumber test is called a feature. Each feature contains steps which tells Cucumber what to do
- __Gherkin:__ It is the name of the syntax
- In order to check the syntax of a file we can use the following command
    cucumber features/test.feature --dry-run

#Keywords

##Feature
* It explains the summary of the test. It does not effect the behaviour of the test
* The text immediately following the "Feature" keyword is the name of the feature
* The remaining lines after the Feature keyword is the description. It cannot contain "Background", "Scenario Outline" or "Scenario"
* Description is the best place to  explain the feature and add the docs and user surveys
 
 ####Example
        Feature: This is the feature title
        
        This is the description of the feature, which can
        span multiple lines.
        You can even include empty lines, like this one:
        In fact, everything until the next Gherkin keyword is included  
        in the description.
* It’s conventional to name the feature file by converting the feature’s name to lowercase characters and replacing the spaces with underscores.
* Feature must be followed by either __Background__, __Scenario__ or __Scenario Outline__ in a valid Gherkin
* A good template for the *description*:
            
            In order to <meet some goal> 
            As a <type of stakeholder> 
            I want <a feature>

##Scenario
It is a single concrete example of how the system should behave under a specific situation.

* Each feature has typically 5-20 scenarios
* Steps in a scenario:
        
            Take system to a particular state ---> Poke it ---> Examine the new state

##Given, When, Then
* __Given:__ It sets the context of the scenario
*  __When:__ It is to interact somehow with the system
*  __Then:__ Checks the outcome of the interaction with expected behaviour

## And, But
We can add more steps to _Given_, _When_, _Then_
* _And_, _But_ do not make a difference to Cucumber. They are there to make the scenario more readable

## Bullets
It can be used to replace _Given_,_When_,_Then_
* It reduces the readability of the scenario a bit
    
## Good Practices
* Each scenario must be independent of other scenarios
* Make sure the scenario names are updated and clearly explain what the scenario does (Use description if necessary)
