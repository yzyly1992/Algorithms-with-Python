## Object-Oriented Programming
2.1 Goals, Principles and Patterns
Intro: Each object in an instance of a class. Each class presents to the outside world a concise and consistent view of the objects that are instances of this class, without going into too much unnecessary detail or giving others access to the inner workings of the objects. The class definition typically specifies instance variables, also known as data members, that the object contains, as well as the methods, also known as member functions, that the object can execute. This view of computing is intended to fulfill several goals and incorporate several design principles, which we discuss in this chapter.

2.1.1 Objbect-Oriented Design Goals
Robustness, adaptability, and reusablility

2.1.2 Object-Oriented Design Principles
Modularity, Abstraction, and Encapsulation

2.1.3 Design Patterns
Patterns for solving algorithm design problems
	- Recursion
	- Amortization
	- Divide-and-conquer
	- Prune-and-search / decrease-and-conquer
	- Brute force
	- Dynamic Programming
	- The greedy method
Patterns for solving software engineering problems
	- Iterator
	- Adapter
	- Position
	- Composition
	- Template method
	- Locator
	- Factory method

2.2 Software Development
Major Steps: Design, Implementation, Testing and Debugging

2.2.1 Design
Responsibilities: divide the work into different actors, each with a different responsibility.
Independence: Define the work for each class to be as independent from other classes as possible.
Behavior: These behaviors will define the methods that this class performs, and the set of behaviors for a class are the interface to the class, as these form the means for other pieces of code to interact with objects from the class.
CRC cards: Class-Responsibility-Collaborator cards are simple index cards that subdivide the work required of a program. The main idea behind this tool is to have each card represent a component , which will ultimately become a class in the program. On the left-hand side of card, we begin writing the responsibilities for this component. On the right-hand side, we list the collaborators for this component, that is, the other components that this componment will have to interact with to interact with to perform its duties.
UML: Unified Modeling Language diagrams are a standard visual notation to express object-oriented software design. 

2.2.2 Pseudo-Code
Pseudo-Code: a mixture of natural language and high-level programming constructs that describe the main ideas behind a generic implementation of a data structure or algorithm.

2.2.3 Coding Style and Documentation
Main Principles: 
	- Python code blocks are typically indented by 4 spaces. It is strongly recommended that tabs be avoided, as tabs are displayed with differing widths across systems, and tabs and spaces are not viewed as identical by Python interpreter. Many Python-aware editors will automatically replace tabs with an appropiate number of spaces.
	- Use meaningful names for identifiers. Try to choose names that can be read aloud, and choose names that reflect the action, responsibility, or data each identifier is naming.
		- Classes should have a name that serves as a singular noun, and should be capitialized."CamelCase"
		- Functions, including member functions of a class, should be lowercase.If multiple words are conbined, they should be separated by underscores(e.g., make_payment). The name of a function should typically be a verb that describes its affect.
		- Names that identify an individual object(e.g., parameter, instance variable, or local variable) should be lowercase noun. Occasionally, we stray from this rule when using a single uppercase letter to designate the name of a data structure (such as tree T).
		- Identifiers that represent a value considered to be a constant are traditionally identified using all capital letters and with underscores to seperate words (e.g., MAX_SIZE).
		- Indentifiers begin with a single leading underscore are intended to suggest that they are only for internal use to a class or module, and not part of a public interface.
	-  Use comments that add meaning to a program and explain ambiguous or confusing constructs. In-line conmments are good for quick explanations. Multiline block comments are good for explaining more complex code sections. Multiline string literals, typically delimited with triple quotes("""), which has no effect when executed.
	- Documentation: Python provides integrated support for embedding formal documentation directly in source code using a mechanism known as a docstring. Formally, any string literal that appears as the first statement within the body of a module, class, or function will be considered to be a docstring.
	- A docstring is stored as a field of the module, function, or class in which it is declared. It serves as documentation and can be retrieved in a variety of ways. The command help(x) produces the documentation associated with the identified object x.

2.2.4 Testing and Debugging
Intro: Testing is the process of experimentally checking the correctness of a program, while debugging is the process of tracking the execution of a program and discovering the errors in it. Testing and debugging are often the most time-consuming acitivity in the development of a program.

