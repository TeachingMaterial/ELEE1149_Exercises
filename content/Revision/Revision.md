# REVISION


Content

[C# Programming](#c-programming)

[Software Process Models](#software-process-models)

[Testing](#testing)

## C# Programming 

1. List and describe four access modifiers in C#. Provide examples of scenarios where each access modifier is commonly used in software development. 

    <details>
    <summary>Answer</summary>

    - The .NET Framework is a software framework developed by Microsoft for building and running Windows applications. It provides a large class library known as the Framework Class Library (FCL) and supports multiple programming languages, including C#.

    - C# is a programming language developed by Microsoft specifically for the .NET Framework. It is a statically typed language that is designed for building a wide range of applications, from simple console applications to complex enterprise-level systems.

    - `Public`: Allows members to be accessed from outside the class or assembly.
    - `Private`: Restricts access to members within the same class.
    - `Protected`: Allows access to members within the same class or derived classes.
    - `Internal`: Limits access to members within the same assembly.

    </details>

2. Identify and describe the four value types and four reference types used in C#. Provide examples of each type and explain their differences in memory allocation and usage

    <details>
    <summary>Answer</summary>

    - Value Types: `Int`, `float`, `double`, `bool`.
    - Reference Types: Classes, interfaces, arrays, delegates.
    - Value types store data directly in memory, whereas reference types store a reference to the memory location where the data is stored.
    - Value types are typically stored on the stack, while reference types are stored on the heap.


    </details>

3. Discuss the purpose of the static keyword in C# and explain why it is incompatible with the keyword "this." Provide examples to illustrate the usage of the static keyword and how it differs from instance members

    <details>
    <summary>Answer</summary>

    - The static keyword is used to declare members that belong to the type itself rather than instances of the type.
    - Static members can be accessed using the type name without the need for an instance.
    - The keyword "this" refers to the current instance of the class, so it cannot be used in static members because static members do not belong to any instance.

    </details>

4. Describe the two naming conventions commonly used in C#: PascalCase and camelCase. Provide examples of scenarios where each naming convention is applied in naming variables, methods, or classes.

    <details>
    <summary>Answer</summary>

    - **PascalCase**: Capitalize the first letter of each word, including the first word. Example: `ClassName`, `MethodName`.
    - **camelCase**: Lowercase the first letter of the first word, and capitalize the first letter of subsequent words. Example: `variableName`, `methodName`.

    </details>


5. Explain the concept of abstraction in OOP. Discuss how abstraction allows developers to focus on essential details while hiding unnecessary implementation complexities. Provide examples to illustrate the use of abstraction in real-world software development

    <details>
    <summary>Answer</summary>

    - Abstraction is a fundamental principle of OOP that involves hiding the complex implementation details of an object and exposing only the essential features or properties.
    - It allows developers to focus on what an object does rather than how it does it, which promotes code **reusability**, **maintainability**, and **scalability**.
    - For example, in a car simulation program, the `Car` class may have methods like `accelerate()` and `brake()`, which abstract away the internal workings of the engine and transmission.

   </details>

---------------------


## Testing 

6. List and describe four types of testing commonly used in software engineering, excluding unit tests, Test Driven Development (TDD), and Behaviour Driven Development (BDD). Provide examples of scenarios where each type of testing is applicable.

    <details>
    <summary>Answer</summary>

    - **Unit Testing**: Verifies individual units or components of the software in isolation, typically at the function or method level.
    - **Automated Testing**: Involves the use of automated tools to execute tests and compare actual outcomes with expected outcomes.
    - **User Testing**: Involves real users testing the software in a real-world environment to provide feedback on usability, user experience, and functionality.
    - **Performance Testing**: Evaluates the performance of the software under various conditions, such as load testing, stress testing, and scalability testing.

    </details>

7. Explain the difference between Test Driven Development (TDD) and Behaviour Driven Development (BDD). Highlight their respective approaches, focus areas, and benefits in software development. 

    <details>
    <summary>Answer</summary>

    - Test Driven Development (TDD): Involves writing tests before writing the actual code. Focuses on unit tests to drive the development process and ensure code correctness.
    - Behaviour Driven Development (BDD): Focuses on defining the behavior of the system from the perspective of its stakeholders. Uses a common language (like Gherkin syntax) to describe features and scenarios, which can then be automated into executable tests.

    </details>

8. Convert the following scenario into the Gherkin syntax for Behaviour Driven Development (BDD):
"An account holder has already inserted their card and will draw £20 cash; they have a balance of £100. The card should be returned to the owner at the end of this transaction from the ATM."

    <details>
    <summary>Answer</summary>

    ```gherkin
    Feature: Withdraw cash from ATM
    Scenario: Account holder withdraws £20 cash
        Given the account holder has inserted their card
        And the account holder has a balance of £100
        When the account holder withdraws £20 cash
        Then the card should be returned to the owner
    ```

    </details>

9. Explain the pattern typically used when writing unit tests. Describe the key components and structure of a unit test, including setup, execution, and assertions. 

    <details>
    <summary>Answer</summary>

    The pattern typically used in writing unit tests includes:

    - **Arrange**: Set up the necessary preconditions and inputs.
    - **Act**: Perform the action or behavior being tested.
    - **Assert**: Verify that the expected outcomes are achieved.

    </details>

10. Consider testing the `Math.Abs()` function in a C# application. Write a comprehensive unit test following the pattern described by yourself above. Ensure that the unit test adheres to the C# naming conventions and covers various test cases for the `Math.Abs()` function

    <details>
    <summary>Answer</summary>

    ```csharp
    [TestClass]
    public class MathAbsTests
    {
        [TestMethod]
        public void Abs_PositiveNumber_ReturnsItself()
        {
            // Arrange
            int number = 5;
            
            // Act
            int result = Math.Abs(number);
            
            // Assert
            Assert.AreEqual(number, result);
        }
        
        [TestMethod]
        public void Abs_NegativeNumber_ReturnsPositive()
        {
            // Arrange
            int number = -5;
                
                // Act
                int result = Math.Abs(number);
                
                // Assert
                Assert.AreEqual(5, result);
            }
            
            [TestMethod]
            public void Abs_Zero_ReturnsZero()
            {
                // Arrange
                int number = 0;
                
                // Act
                int result = Math.Abs(number);
                
                // Assert
                Assert.AreEqual(0, result);
            }
        }
    ```
    </details>


-----------------

## Software Process Models

11.  Discuss why it is usually cheaper to use software engineering methods and techniques in developing software systems, considering that software costs more to maintain than to develop. Highlight the role of proper planning, design, and implementation in reducing maintenance costs

    <details>
    <summary>Answer</summary>

    - Proper planning and design reduce the likelihood of defects and rework, minimizing maintenance costs over the software's lifecycle.
    Systematic development processes, such as requirements analysis, design, and testing, help identify and address issues early, reducing the risk of expensive corrective actions later.
    - Reusable components, modular design, and automation in development increase productivity and efficiency, resulting in lower development costs overall.

    </details>

12.  Compare and contrast plan-driven and agile processes in software development. Discuss their respective approaches, principles, and advantages, as well as their suitability for different project types and environments.

    <details>
    <summary>Answer</summary>

    - **Plan-Driven Processes**: Also known as traditional or waterfall approaches, plan-driven processes emphasize extensive upfront planning, documentation, and sequential execution of project phases. They are well-suited for projects with stable requirements and clear objectives but may struggle to accommodate changes or uncertainties.

    - **Agile Processes**: Agile methodologies, such as Scrum or Kanban, prioritize flexibility, collaboration, and incremental delivery. They emphasize iterative development, adaptive planning, and continuous improvement based on customer feedback. Agile processes are suitable for projects with evolving requirements, dynamic environments, and a need for frequent stakeholder engagement.

    </details>