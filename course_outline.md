# GoBridge workshop
# Go for Complete Beginners
This workshop is designed to teach complete beginners (people with no coding experience) programming principles using Go. 

It is planned for 6 meetings of 3 hours each, including a short break, based on the workshop that was held in Berlin on 09-11/2016. We met every other week, and in-between the instructors were available on the Gophers slack to answer questions.

The content is an adjustment of How I Start to be complete-beginner friendly, with the kind permission of Peter Bourgon.

To see the table of content menu on the left side of the screen click Tools -> Document outline
Alternatively you can see the TOC in the next page.

### How to read this guide
Most weeks have a theoretical part and a practical part
The theoretical part should be discussed in a group, and the instructor can show an example. Each bullet point and sub-point should be mentioned and clarified.
The practical part can take place in the playground or locally, depends on the week. Each bullet point and sub-point should have an exercise or two done by each participant. As those are mostly basic elements of the language, the instructor is encouraged to think of local version. For example, practice the fmt library to print a sentence relevant to the recent news.
The homework part are exercises the participants will do at home between the meetings to repeat the material and can ask about on slack.

### Instructing tips
Asking “is all clear?” or “who didn’t understand?” is not enough. Many participants are shy or afraid to ask a stupid question. Some approaches that worked in the Berlin chapter:

- Remind there are no stupid questions here
- Thanking and responding that it was a good question
- Speak slowly and repeat the keywords - both new and previous terms
- Get the other instructors to walk in the class and ask each participant at least once during the meeting “what questions do you have?”
- When a difficult technical question is asked in the group discussion, invite the person to discuss this during the break



# Meeting #1 - Intro to Programming & Go
## Theory
### Intro to go
- Where go fits in the field of languages the participants know
- When and for what purpose was it invented
- What version is current
- Parallelism vs concurrency (simple gophers example from Rob Pike’s talk)
- Why people like it (concurrency, simplicity, mascot)
- What are keywords (name some that may be familiar: var, const, if, else)
- Lexical identifiers (How to comment, no need for semicolons, how to format)
- Some notes on compilers and the go compiler:
All programs have to be converted to a form that the computer understands. Some languages, like Python and Ruby, do this as you run the program. Other languages, like Go and C, require a special step: compiling.
- The Go Community is awesome (GoBridge, Women Who Go, Newsletter, meetups, twitter, confs, slack, etc.)
- Sign up to gophers slack and make sure everyone are in a dedicated channel

## Practice at the playground
### Variables
- Basic types: String, int, float, bool, slices (glimpse, saying we’ll focus later)
- Zero values
- Different declaration formats
- Constants

### Functions
- Signature meaning
- Caller
- Name (repeat naming conventions)
- Return values (go has multiple, not all languages have that)
- Call a function in main

## Homework
For this homework guide the class to edit the playground exercises, as imports are introduced in class #3, but imports are already used now. If they ask - explain shortly, say this will be introduced later and encourage independent reading at home.
4 functions for the 4 mathematical operation
Func that receives name, and prints a message+name
Func that receives your age and name, and prints “<name> you were born in <year>”



# Meeting #2 - Go basics
## Practice in playground
### Loops
- For
 - Standard
 - While
 - Infinite
- If-else
- Switch
 - Standard
 - Break
 - Fallthrough
 - Single case with several options
 - No condition
- Defer
 - Defers are called as FILO
- Pointers
 - Value type (point to value in memory) vs. reference type (contains the address of the val)
 - Slices and arrays

Do some exercises with fun visual libs like strings, math, fmt

## Homework
- Guessing game: func that gets number of guesses for the current round, chooses a random number, and for <number of guesses> times, the user attempts to guess the random number, and the game prints yes/no
- Func that gets an operator and 2 numbers, and prints the result of the operation on the two numbers
- Func that gets 5 numbers and prints their average (basically implement average)



# Meeting #3 - First full program
## Environment setup
- Installing and setting Gopath
For reference you can use Bill’s post
- IDE
- Github account


## Practice locally
### Packages
- Naming conventions for params and functions
- Program structure 
Why should there be one
Standard: main, helper functions
- Folder/directory is a package
This is where helper functions go
- Exports (private/public)
- Import	

Exercise: Write a hello world

### Testing
- Importance of testing
- How to do test driven development
- Testing the math funcs we did so far

### Homework
- Implement the exercises from hw#1 and hw#2 locally
- Use one of the hash libs, for example md5, and see how your name/address/etc look like when they are hashed



# Meeting #4 - Making a web server
Here we’re starting to follow the online tutorial
## Theory
### Localhost
- Localhost
- Overview how websites are hosted and served
- Localhost vs. online website

### What is web client/server
- Package net/http
- What is web client/server
- What is http handler
- Encoding, decoding, escaping

### API Server
- What is an API?
- Demo some fun APIs like Google Vision, IBM Watson, Microsoft Cognitive Services

## Practice locally
### Localhost
- Write a local hello world
- Adding routes
e.g. “/name” prints “hi <name>”

### API Server
- Sign up to the weather API service and understand their response format
- Read and plan struct that will match the API response

## Homework
- Func that gets string as input and prints the encoding of it, decodes back and prints that. Try those on different urls, especially values like wikipedia values in foreign languages
- Add more routes locally



#Meeting #5 - Weather API consumption
## Theory
### API Server
- Maps
- Struct
Slow down here, explain slow and in detail, and include an example exercise in class (in addition to the homework)
- Methods
- Interfaces

### Web services
- JSON
- Decoding the request
- Responding
- Field tags (json:”name”)
- Marshaling and unmarshaling
How the body from the request is filled in the struct

## Practice locally
### API Server
- Build response struct
- Query the weather API 
- Unmarshal json
- Convert Kelvin -> Celsius/Fahrenheit
- Display response

## Homework
- See what happens when you add to the struct fields that are not in the API
- Define a struct to define a person, populate it, marshal and print the values, unmarshal and print the values




# Meeting #6 - Graduation event
## Going online
- First hour for last questions and fixes
- Upload the code to GitHub
- Demo to classmates
- Consider bringing a motivation speaker
- Introduce further GoBridge material
- Suggest attending meetups
- Remind to keep using slack
