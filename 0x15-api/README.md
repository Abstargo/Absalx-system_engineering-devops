## 0x15. API

### Background Context
Old-school system administrators usually only know Bash and that is what they use to build their scripts. While Bash is perfectly fine for a lot of things, it can quickly get messy and not efficient compared to other programming languages. The new generation of system administrators, usually called SREs, are pretty much regular software engineers but instead of building products, they are managing systems. And one of the big differences with their predecessors is that they know more than just Bash scripting.

One popular way to expose an application and dataset is to use an API. Often, they are the public facing part of websites and micro-services so that allow outsiders to interact with them – access and modify their data. In this project, you will access employee data via an API to organize and export them to different data structures.

This is a perfect example of a task that is not suited for Bash scripting, so let’s build Python scripts.

### General


1. **What Bash scripting should not be used for**:
   Bash scripting is not suitable for tasks that require complex data manipulation or heavy processing. It's not ideal for building large-scale applications or handling tasks that require high performance or extensive error handling. Bash scripting is best suited for automating repetitive tasks, simple system administration tasks, and small-scale utilities.

2. **What is an API**:
   API stands for Application Programming Interface. It is a set of rules, protocols, and tools that allow different software applications to communicate with each other. APIs define the methods and data formats that applications can use to request and exchange information. They enable the integration of different systems, services, and functionalities, allowing developers to leverage existing code and services in their own applications.

3. **What is a REST API**:
   REST API (Representational State Transfer API) is a type of API that follows the principles of REST architectural style. REST APIs use standard HTTP methods (such as GET, POST, PUT, DELETE) to perform operations on resources. They are stateless, meaning each request from a client contains all the information necessary for the server to fulfill the request. REST APIs typically use JSON or XML as their data format and are widely used for building web services and interacting with web applications.

4. **What are microservices**:
   Microservices is an architectural approach to developing software applications as a collection of loosely coupled, independently deployable services. Each service in a microservices architecture is focused on a specific business capability and can be developed, deployed, and scaled independently. Microservices communicate with each other through APIs and often use lightweight protocols like HTTP or messaging queues. This approach enables organizations to build complex applications more easily, improve scalability, and facilitate faster development and deployment cycles.

5. **What is the CSV format**:
   CSV stands for Comma-Separated Values. It is a plain text format used to represent tabular data, where each line in the file represents a row of data, and the values within each row are separated by commas (or other delimiters, such as tabs or semicolons). CSV files are commonly used for exchanging data between different software applications, especially in scenarios involving spreadsheets or databases.

6. **What is the JSON format**:
   JSON stands for JavaScript Object Notation. It is a lightweight data interchange format that is easy for humans to read and write and easy for machines to parse and generate. JSON is often used to represent structured data, such as objects and arrays, and is commonly used in web development for transmitting data between a server and a web application. JSON is based on a subset of the JavaScript programming language, but it is language-independent and can be used with any programming language.

7. **Pythonic Package and module name style**:
   Package and module names in Python should be lowercase, with underscores (_) as word separators. For example, `my_package`, `my_module`.

8. **Pythonic Class name style**:
   Class names in Python should follow the CapWords convention, also known as CamelCase, where each word in the name is capitalized and there are no underscores between words. For example, `MyClass`, `MyAwesomeClass`.

9. **Pythonic Variable name style**:
   Variable names in Python should be lowercase, with underscores (_) as word separators. For example, `my_variable`, `my_awesome_variable`.

10. **Pythonic Function name style**:
    Function names in Python should be lowercase, with underscores (_) as word separators. For example, `my_function`, `calculate_sum`.

11. **Pythonic Constant name style**:
    Constant names in Python should be uppercase, with underscores (_) as word separators. For example, `MAX_SIZE`, `PI`.

12. **Significance of CapWords or CamelCase in Python**:
    CapWords or CamelCase convention is used in Python to make class names and other identifiers more readable and distinguishable. It helps improve code readability and maintain consistency across different parts of a program. By following this convention, it's easier for developers to identify classes, functions, and other components in Python code.
