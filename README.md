docker-compose -f docker-compose-local.yml rm -s -f backend;
cd bac-nd;
./buil-sh;
cd ..;
docker-compose -f docker-compose-local.yml up -d;






























# ST-EXAM INVENTORY

## Threads
Q1\
Sequence diagrams illustrate interactions between objects on a time axis going from the top to the bottom of the diagram. The lifeline of an object is the dashed line. The messages passed (that is, the method calls) between the objects are shown as the arrows. On the figure the arrows denote locking resources. We know that both threads need both resources. 
 
                                       
At which method call can we be sure that there is a deadlock? 

Q2\
What will be the result of calling the wait() method of an object if the calling thread doesn't posess the monitor lock? 
Q3\
What is the default priority of threads? 
Q4\
Which possible outputs can this running code produce? 
```
public class Tester extends Thread {     
    int code = 9;     
    public void run() {         
        this.code = 7; 
    }     
    public static void main(String[] args) {
        Teste-thread = new Tester();
        threa-start();
        for (int i = 0; i < 5; i++-{
            System.out.print(threa-code); 
        } 
    } 
} 
```
Q5\
What will be the result when running this code? 

```
public class MyThread extends Thread {     
    volatile private int x = 3; 
    public static void main(String[] args) throws Exception {
        new MyThread().foo(); 
    }     
    public MyThread() {
        x = 10;
        start(); 
    } 
    public void foo() throws Exception {
        join();
        x = x - 1; 
        System.out.println(x); 
    } 
    public void run() { 
        x *= 2;
    } 
} 
```
Q6\
What will be the result when running this code? 
```
public class Test extends Thread {     
    public void run() { 
        System.out.println(isAlive()); 
    } 
    public static void main(String[] args) {
        Test test = new Test(); 
        System.out.println(test.isAlive());
        test.run(); 
    }  
}
```
Q7\
Which of these are atomic operations?\
- Reading/writing reference variables\
- Reading/writing of all primitive types\
- Both\
- None of the above\

Q8    
Which statement is true of this code?
```
public class Test extends Thread {
    private static int x;
    public synchronized void foo() {
        int current = x;
        current++;
        x = current; 
    } 
    public void run() {
        foo();
    }
} 
```
- We can make the class thread-safe, if we make the run method synchronized.\
- The class is thread-safe.\
- We can make the class thread-safe, if we make the foo method static.\
- This code throws an exception at runtime.\

Q9
Which of these statements about immutable classes is not true?\
- The class should be final to avoid inheritance.\
- All the attributes of the class should be declared as private final.\
- We have to make a copy of the objects stored in attributes, when we return it in a getter method.\
- The class should not contain any kind of methods, that change the state after the constructor.\
 
## JDBC 
Q1\
Which of these SQL statements are DML statements?\
- update [table] set ...\
- delete from [table] ...\
- alter table ...\
- insert into [table] ...\

Q2\
Which of these is an incorrect way to access the data in a ResultSet?\
- String value0 = rs.getString(0);\
- String value1 = rs.getString(1);\
- int    value2 = rs.getInt(2);\
- int    value3 = rs.getInt(“ADDR_LN1");\

Q3\
What information cannot be obtained from the SQLException object?\
- SQL status code.\
- Driver / Database specific error code.\
- Database request causing the error.\
- Description of the error that occurred.\

Q4\
Which of the following statements is true?\
- CallableStatement extends the PreparedStatement interface. This interface can be used to call SQL stored procedures.\
- Statement extends the PreparedStatement interface and is used when the SQL query does not need to be run multiple times.\
- PreparedStatement is used to start static queries (eg select * from table), therefore PreparedStatements cannot be parameterized.\
- Batch processing of SQL statements is possible using PreparedStatement.\

Q5\
How to start a new database transaction?\
- By requesting a Transaction object from Connection and calling that begin () method.\
- By requesting a Transaction object from Connection and setting its autoCommit property to false.\
- By calling the beginTransaction method of the Connection.\
- By setting the autoCommit property of the Connection to false and executing an SQL statement.\
 
Q6\
When do we use the transaction on databases?\
- To run stored procedures\
- To perform multiple operations atomically\
- For a linked table query\
- To name transfers\

Q7\
Which connection is usually interpreted with a connection table?\
- 1-n connection\
- m-1 connection\
- m-n connection\
- D connection\

Q8\
Which one is not part of the Entity-Relationship diagram?\
- Attribute\
- Entity\
- Keys\
- Class\

Q9\
Which one is not true about the relationship between JTable and the model?\
- JTable does not contain data\
- The model can be redefined\
- The model cannot notify JTable of the change\
- The representation of the model may differ from the data queried by JTable\
 

## Software Technology / UML 
Q1\
What are the principal quality metrics of software?\
- Delivery time, implementation cost, hardware and software requirements.\
- Maintainability, reliability, safety, efficiency, usability.\
- Modifiability, Extensibility, Resolution, Reusability, Reliability.\
- Ergonomics, usability, compatibility, hardware and software requirements.\
 
Q2\
Which of these is the structure of a user story?\
- USER … IN USE CASE … WITH RELATION …\
- AS A … USE … TO …\
- WHEN … APPLYING … IN ORDER TO …\
- GIVEN … WHEN … THEN …\

Q3\
What is the correct order of requirements analysis steps?\
- feasibility analysis, requirement exploration, requirement specification, requirement validation\
- requirement exploration, requirement specification, requirement validation, feasibility analysis\
- requirement exploration, requirement validation, requirement specification, feasibility analysis\
- requirement exploration, requirement specification, feasibility analysis, requirement validation\
 
Q4\
Which of these is not a software development process?\
- waterfall\
- 	evolution\
- scrum\
- 	prototyping\

Q5\
Which of these are the relations of a UML use case diagram?\
- dependency, composition, usage, nesting\
- precedes, include, usage, generalization\
- usage, nesting, import), dependency\
- interface, implementation, include\

Q6\
What is the UML deployment diagram used for?\
- Describe the sequence of steps required to install the software on a given machine.\
- It depicts all the error possibilities that you may encounter during installation.\
- Describe the software components according to how to install them in an installation package.\
- Depict the physical placement of software components (on different machines) with the required software environment.\

Q7\
Which OOP design principle is violated by the singleton design pattern? The singleton pattern guarantees that there is only a single instance created from a class which can be accessed through a static method.\
- Single Responsibility Principle\
- Open/Closed Principle\
- Liskov Substitution Principle\
- Dependency Inversion Principle\
 
Q8\
Which of these techniques can be used to implement dependency inversion?\
- observer\
- MVC (modell-view-controller)\
- dependency injection\
- generalization\
 
Q9\
What is Test Driven Development (TDD)?\
- A software development method in which tests are written before the actual program code is written.\
- Test method to ensure that test cases cover all program units and are performed in the appropriate order.\
- A general principle that states that all instructions in program code should be verified using unit tests (100% code coverage).\
- A testing method in which unit tests are first performed on classes (and their methods), then integration tests are used to check the combined behavior of the classes, and finally system tests are used to check the behavior of the entire software.\
 
Q10\
Which the following features is not provided by unit testing frameworks?\
- Create manual test cases in separate program units (classes).\
- Generate test cases automatically, that covers all scenarios, by analyzing the code.\
- Assert statements, which compare the expected and the return values.\
- Creation of test reports, which lists the passed/failed tests.\

Q11\
In the case of Unit testing, the parts of the program must be separated from each other and boundaries must be established between them. One possible solution to this is to use objects that mimic the behavior of other objects. What are these objects called?\
- Mock objects\
- Modules\
- Units\
- Atoms\

Q12\
What is the starting point of object-oriented design?\
- 	Functions\
- 	Activities\
- 	Entities and relations\
- 	Architecture\

Q13\
How do we express that an object is related to several objects of a class? 
- With composition\
- With multiplicity\
- With an array type attribute\
- With aggregation\

Q14\
Which of these can we assign constraints to on a class diagram?\
- 	Relation\
- 	Attribute\
- 	Method parameters\
- 	All\
 
Q15\
Which of these relations is between classes?\
- 	Association\
- 	Dependency\
- 	Inheritance\
- 	Aggregation\

Q16\
Which diagram is not part of the dynamic model?\
- State diagram\
- Sequence diagram\
- Activity diagram\
- Component diagram\

Q17\
What cannot have a state on a state diagram?\
- Name\
- Invariant\
- Precondition\
- Parameter\


Q18\
Which method can reduce the complexity of the state diagram?\
- Generalization\
- Aggregation\
- By generalization and aggregation\
- None of the others\

Q19\
Which statement is true?\
- The invariant of generalization is the disjunction of the invariants of states\
- The invariant of generalization is the conjunction of the invariants of states\
- The invariant of aggregation is the disjunction of the invariants of states\
- The states obtained by the two methods have no invariant

Q20
Which diagrams are part of the static model?\
- Class Diagram, Object Diagram\
- Class Diagram, State Diagram\
- Object diagram, Sequence diagram\
- Object Diagram, Activity Diagram
 
Q21\
Based on the following implementation, which relationship exists exactly between the car and the engine?
```
public class Car { 
    private Engine engine; 
    public Car(Engine engine){          
        this.engine = engine; 
    }  
    public Engine getEngine(){
        return engine; 
    } 
} 
```
- Association\
- Aggregation\
- Composition\
- Generalization

Q22\
Based on the following implementation, which relationship exists exactly between the car and the engine?
```
public class Car { 
    private final Engine engine; 
    public Car(int engineCapacity, int engineSerialNumber) { 
        this.engine = new Engine(engineCapacity, engineSerialNumber);
    }      
    public int getEngineCapacity() {
        return engine.getEngineCapacity(); 
    }  
    public int getEngineSerialNumber(){
        return engine.getEngineSerialNumber(); 
    } 
} 
```
- Association\
- Aggregation\
- Composition\
- Generalization
 
Q23\
What is the relationship between the Person and Phone classes in the class diagram below?\
- Association\
- Aggregation\
- Composition\
- Generalization 
 
## Implementation related questions 

Q1\
What kind of methods do we have to implement when we would like to use instances of our own class as keys in a HashMap?\
- == operator\
- hashCode(…) method\
- equals(…) method\
- hashCode(…) and equals(…) methods
 
Q2\
Which of the following options should you choose if you want to apply mainly an index-based search to a dynamically changing data set where the same element can occur more than once? (We only want to add a new item to the end of the collection, we don't want to delete it from the collection often.)\
E. ArrayList\
F. LinkedList\
G. Array\
H. HashSet 

Q3\
Which implementation to choose from the following options if you want to use a collection that does not contain duplicate items and you do not need to store the items in the order of insertion or in ascending order of values?\
- List\
- TreeSet\
- LinkedHashSet\
- HashSetArrayList 

Q4\
Which of the following implementations of interfaces are used to store key-value pairs? A List\
- Set\
- Map\
- Collection

Q5\
Which of these statements is true?\
- A final abstract class must have at least one abstract method\
- An abstract class has at least one abstract method\
- All the attributes of a final class are final\
- The derived class of an abstract class can be also abstract 
 
Q6\
Which of these statements is false?\
- We cannot derive from a final class\
- Interfaces cannot be derived\
- A class can implement multiple interfaces\
- We have to implement all methods of the interface 
 
Q7\
Which of these can be a generic parameter?\
- Primitive type\
- Class\
- Interface\
- Class, that implements the methods used in the generic 
 
Q8\
Which collection can be indexed?\
- HashSet\
- HashMap\
- Vector\
- TreeMap 
 
Q9\
What can be static in JAVA?\
- Class field\
- Method\
- Class / interface\
- Enumeration

Q10\
What does Java support about multiple specialization and multiple generalizations?\
- Generalization\
- Specialization\
- Both\
- None 

## Software development methodologies and models 

Q1\
Which of the following is not an agile principle?\
- Prefer the methodology instead of the tools\
- Prefer the operating software instead of a comprehensive documentation\
- Prefer cooperation with the client instead of enforcing the contractual negotiations\
- Prefer responding to changes instead of following the plan. 
 
Q2\
Which statement is not true about the sprint?\
- The product is all designed, coded and tested within the sprint.\
- The result of the sprint is a working code representing business value.\
- Once tasks and times have been defined, only the product owner will be involved in the work of the team.\
- The Scrum team works in a self-organizing way throughout the sprint. 

Q3\
Which statement is true for the Scrum Master? (not included)\
- Scrum Master is the manager of the Scrum team\
- The Scrum Master leads the daily Scrum\
- Scrum Master is not responsible for protecting the work of the SCRUM team from outside influences\
- Scrum Master is responsible for the processes 
 
Q4\
Which statement is true for daily Scrum? (not included)\
- The daily Scrum is led by the Scrum Master.\
- During the daily Scrum, team members report to the Scrum Master on their progress.\
- During the daily Scrum, the goal is to remove obstacles that affect the team.\
- The daily Scrum can last up to 15 minutes.

Q5\
Test-driven development (TDD) is a software development methodology according to which…\
- the tests must be written before the actual program code is implemented.\
- tests must be performed on each unit after the actual program code has been implemented.\
- new program code can be implemented after approval by the test colleague.\
- the test report must be assigned to the documentation one day before the implementation of the new program code. 
 

## Version control 
 
Q1\
What is the purpose of the continuous integration (CI) practical method?\
- Immediate, automated filtering of possible errors and integration problems, feedback to the developer. (Self-check build)\
- Automatically re-run failed integration tests until they are repaired.\
- Facilitates the transition to an object-oriented programming language.\
- Complete replacement of manual testing. 
 
Q2
What are the disadvantages of centralized version control systems (Example: SVN, Perforce, CVS)?\
- The privileged role of the server. (In the event of a failure, the system becomes unusable until the server is repaired.) In addition, version control requires a network connection.\
- File-based operation\
- Local storage\
- Concurrency management realized by exclusive locks. 
 
Q3\
Which statement is not true for distributed version control systems (Example: Git, Mercurial)? 
- A decentralized, distributed network model is used, where concurrency management is typically done through post-submission merging.\
- Each client has a complete repository and version history. The operations of the revision management tool take place locally on the client's storage.\
- Communication is peer-to-peer, but it is also possible to set up dedicated servers.\
- A set of file-based operations is typical, where concurrency management is typically done by merging before submission. 

Q4\
Is it true that there can be no conflict with Git merge?\
- True, as conflict can only occur with rebase.\
- False, because there is a conflict between colleagues for every merge.\
- True, since each merge is also another commit.\
- False, as git may not be able to resolve changes automatically. (Example: Two different commit stores a change on the same line in a file.) 

Q5\
Which of the following are the build tools?\
- Ant, Maven, Gradle\
- Ant, Git, Subversion (SVN)\
- Ant, Maven, Subversion (SVN)\
- Maven, Gradle, Git\
 
## Design principles, Design patterns 

Q1\
What does the DRY principle say?\
- Don’t implement code in advance that “will need it in the future” because we will almost certainly never need it.\
- Each piece of knowledge must have a single, clear and reliable representation within a system.\
- Perfection is not best approached when we can no longer add anything to a system, but when we do not know what to take from it.\
- It is safe to say that the quality of our code base will improve if we always leave our current code there a little “better”, a little cleaner than we found it.
 
Q2\
Which object-oriented principle is violated in the code snippet below?
```
public enum Status { 
    UNRESOLVED, IN_PROGRESS, RESOLVED, CLOSED 
}  
public class Task { 
    protected Status status; 
    public void close() { 
        this.status = Status.CLOSED; 
    } 
}  
public class ProjectTask extends Task { 
    @Override 
    public void close() { 
        if(status == Status.IN_PROGRESS) {  
            throw new RuntimeException("You cannot close …"); 
        } 
        super.close(); 
       } 
 } 
```
- Liskov Substitution Principle\
- Dependency Inversion Principle\
- KISS\
- DRY 

Q3\
Which of the following is not a SOLID principle?\
- Liskov Substitution Principle\
- Open / Closed Principle\
- Single Responsibility Principle\
- Separation of Concerns Principle
 
Q4\
Which object-oriented principle is violated in the code snippet below?
```
public class DamageCalculator {
    private int damageFactor; 
    public DamageCalculator(int damageFactor) {
        this.damageFactor = damageFactor; 
    } 
    public int totalDamage(int baseDamage, int damageAlgorithm){
        switch(damageAlgoritm) { 
            case 0: 
                return baseDamage * damageFactor;
            case 1:
                return baseDamage * 4;
            default: return baseDamage; 
        } 
    } 
} 
```
- Dependency Inversion Principle\
- Open/Closed Principle\
- Interface segregation Principle\
- Liskov Substitution Principle

Q5\
Given a Lamp class. The lamp has a color and can be switched on / off. In our apartment there is a switch on the wall, which was implemented as follows. What could be the problem with this implementation?
```
public class Switch {
    private Lamp lamp; 
    public Switch(Lamp lamp) {
        this.lamp = lamp; 
    }
    public void useSwitch(){
        if(lamp.isOn()) {
            lamp.turnOff(); 
        } else { 
            lamp.turnOn(); 
        } 
    } 
} 
```
- The switch violates the Liskov Substitution Principle\
- The switch violates the Open/Closed Principle\
- The switch is at a higher abstraction level than the lamp, so it violates the Dependency Inversion Principle\ 
- The switch violates the Single Responsibility Principle

Q6\
Which design pattern provides a solution to the problem of notifying multiple objects when another object changes state.\
- Singleton\
- Observer\
- Adapter\
- Factory 

Q7\
Which design pattern can be used to avoid constructors with long parameter lists?\
- Observer\
- Factory\
- Builder\
- Command 

Q8\
Which design pattern implementation can be recognized in the following code snippet?
``` 
public MyPattern withName(String name) {
    this.name = name;
    return this; 
}  
public MyPattern withNumber(int number) {    
    this.number = number;    
    return this; 
} 
```
- Singleton\
- Builder\
- Command\
- Adapter

Q9\
Which design pattern can we use if we want to provide an interface for creating a family of related or interdependent objects without specifying a specific class?\
- Factory method\
- Adapter\
- Builder\
- Abstract Factory

Q10\
Which design pattern can be used in case we want to transfer the instantiation of a given class to the corresponding subclasses?\
- Factory method\
- Builder\
- Command\
- Observer 
 
Q11\
Which design pattern does the following code snippet implement?
```
public class MyPattern {
    private MyPattern(){} 
    private static class MyPatternInstance { 
        private static final MyPattern INSTANCE = new MyPattern(); 
    } 
    public static MyPattern getInstance() {
        return MyPatternInstance.INSTANCE;  
    } 
} 
```
- Singleton\
- Factory\
- Builder\
- Adapter 

Q12\
Which design pattern does the following code snippet implement?
```
public abstract class Maze { 
    private final List<Room> rooms = new ArrayList<>(); 
 
    public Maze() { 
        Room room1 = makeRoom();        
        Room room2 = makeRoom();         
        room1.connect(room2);         
        rooms.add(room1);         
        rooms.add(room2); 	 
    } 
    protected abstract Room makeRoom(); 
}  
public class MagicMaze extends Maze {
    @Override 
    protected Room makeRoom() {         
        return new MagicRoom(); 
    } 
} 
```
- Factory method\
- Command\
- Adapter\
- Abstract Factory 
