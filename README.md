Individual project: CMPE 202

Name: Vamsi Agnihotram,	Student ID: 016920709

GitHub Link : https://github.com/gopinathsjsu/individual_project_vamsiA/tree/main


1. Describe what is the primary problem you are trying to solve. 
Ans: Primarily, I need to figure out how to verify if a credit card is authentic or not by matching it with different card types like Mastercard, Visa, American Express, and Discover. This involves using the credit card number to identify the issuing company and determining the correct objects depending on the card type.
 

2. Describe what are the secondary problems you try to solve (if there are any).
Ans: The secondary challenge involves choosing the right design patterns, and considering the future integration of new credit classes for different types of credit cards.
 
3. Describe what design pattern(s) you use (use plain text and diagrams).
Ans: Design Patterns: Chain of Responsibility, and Strategy
 
Strategy Design Pattern:
 
The Strategy Design Pattern facilitates changing an application's behavior dynamically through a chosen strategy. This pattern permits the creation of distinct objects and strategies for various file types, thereby adapting the application's functionality as needed.
 
I employed the Strategy Design Pattern in my application to accommodate a variety of file formats. I designed three interfaces - Reader, Writer, and CreditCardHandler - to handle different aspects of file processing and credit card handling.

The Reader interface establishes a standard agreement for classes designed to read input files, featuring a readFile method that manages the reading operation according to the type of the input file.

The CreditCardHandler interface defines a common structure for classes responsible for checking the credit card type of parsed input files. It includes a checkCreditType method that takes the parsed input file and determines if it belongs to any specific credit card type category.

The Writer interface offers a unified framework for classes tasked with writing data to various file formats. It encompasses a writeToFile method, which accepts an OutputEntry type input (symbolizing the ultimate output format) and records the data in the desired file format.
 
This design pattern enables runtime behavior swapping and follows the Open/Closed principle. It allows for the introduction of new strategies without affecting the client code, making it easy to accommodate new file formats without disrupting the existing code or design.
 
Chain of Responsibility Design Pattern:
 
Once an XML, JSON, or CSV file is parsed, its content must be validated to identify the type of credit card from the four available options.
 
The Chain of Responsibility design pattern can be employed to check the file against various credit card handlers. The process begins with the MasterCard handler, and if the file fails to meet MasterCard's criteria, it moves to the next handler in the sequence. This approach enables adaptable and scalable verification for multiple types of credit cards.

To streamline the process, a main credit card handler is introduced to serve as a mediator. It takes the file and forwards it to the respective credit card handlers for validation. Every handler adheres to the main handler's protocol, conducting checks pertinent to its specific credit card type. This method ensures a consolidated and systematic validation, enabling each handler to concentrate on its assigned credit card type.
 
4. Describe the consequences of using this/these pattern(s)?
 
Chain of Responsibility
 
Advantages:
 
-> Decouples the sender of a request from its recipients.
 
-> The client is unaware of the chain structure and interacts with the chain through direct method calls.
 
-> The order of the chain can be easily modified or adjusted, and new handlers can be added or existing ones can be removed as needed.
 
Disadvantages:
 
-> Debugging and observing the runtime characteristics of the chain can be challenging due to the dynamic nature of the pattern.
-> If the chain is not properly configured or there are gaps in the chain, it may lead to requests being ignored or not processed correctly.
 
      2. Strategy Design Pattern: 
 
Advantages:
 
-> The Strategy design pattern provides flexibility in adding new strategies as needed without impacting existing code.

-> It promotes code reusability. By encapsulating specific algorithms or behaviors into separate strategies, these strategies can be reused across different parts of the application. This eliminates the need for duplicating code or implementing similar logic multiple times, leading to cleaner and more maintainable code.
 
Disadvantages:
 
-> Users of the Strategy design pattern should be aware of multiple strategies and understand the distinctions between them.
 
-> Having a large number of objects at the same time can become cumbersome and redundant in the Strategy design pattern.
 

How to Run the project:

Run the App.java 

Enter the input file path: Input file path with extension

Enter the output file path: Ouput file path with extension
 
How to test Junit test?
 
Click on Run all tests to check JUnit test cases.


UML Class Diagram: 

Separate file in GitHub Repo.




