#Cucumber

- The default folder for features in cucumber is `features`
- __feature:__ Each Cucumber test is called a feature. Each feature contains steps which tells Cucumber what to do
- __Gherkin:__ It is the name of the syntax
- In order to check the syntax of a file we can use the following command
 
    cucumber features/test.feature --dry-run
- `# language: fr` can be added to the beginning of feature to change the langiuage to French
- `cucumber --i18n help` shows the list of available languages
- `cucumber --i18n fa` shows the list of available commands in that language (Persian in this case)
- In Ruby regular expressions are placed inside two "/" (example /This is a test regular expression/)
- When starting a regular expression with pranthesis, it becomes a capture group
- __alteration:__ When we express different options in regular expression using "|" `Given /I have deposited \$(100|250) in my Account/ do |amount|`
- __The Dot:__ It means any single character in regular expression
- __ The Star:__ It takes a character (or metacharacter) and tells us how many times it can bre repeated
- __Chacracter Classes:__ It tells us to match one of a range of characters. They are allways inside a square bracket `Given /I have deposited \$([0-9]*) in my Account/ do |amount|`
- __ The Plus:__ It means at least one
- \d stands for digit, or [0-9].
- \w stands for word character, specifically [A-Za-z0-9_]. Notice that underscores and digits are included but not hyphens. 
- \s stands for whitespace character, specifically [ \t\r\n]. That means a space, a tab, or a line break. 
- \b stands for word boundary, which is a lot like \s but actually means the opposite of \w. Anything that is not a word character is a word boundary. 
- You can also negate shorthand character classes by capitalizing them, so for example, \D means any character except a digit.


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
* Make sure the scenario names are updated and clearly explain what the scenario does (Use descriptin if necessary)
* There are typically several step definition files in step-definiton folder
* Separate file per domain entity so that step definitions that work with similar parts of the system are kept together
* Cucumber ignores keywords when matching a step (_Given_, _When_ amd _Then_ are all the same for cucumber in terms of regular expression)
* The best way to avoid ambiguity with mathcing regular expressions is to pay attentiion to precise wording of your steps

## Comments
* They start with "#"
* They need to be the first and only thing in the line (Except for white lines)

## Step and Step Definition
* __Step:__ Each _scenario_ is made of a series of steps which are written in plain language
* __Step Definition:__ It is a piece of Ruby code which tells cucumber what to do for a particular step
