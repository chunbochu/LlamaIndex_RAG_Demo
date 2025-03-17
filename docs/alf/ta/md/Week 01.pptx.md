# FRANKLIN UNIVERSITY

# COMP 611

# Week 01

© 2021 Tim Kington, Todd Whittaker

FRANKLIN UNIVERSITY

FOUNDED 1902
---
# Introductions

# FRANKLIN UNIVERSITY

WWW franklin edu
---
# Administrivia

# COMP 611: Advanced Data Structures and Programming

This course covers key knowledge and skills for advanced software development using the object-oriented approach. The student learns, manipulates and reflects on nonlinear data structures such as trees and heaps. Recursive algorithms, sorting algorithms, algorithm efficiency, and advanced design patterns are addressed.

To support the advanced concepts and principles of software development, the student will design, code, test, debug, and document programs with increased scale and complexity using industry’s best practices (such as GitHub) and the Java programming language.
---
# Administrivia

# Course Outcomes

1. Implement and use Sets.
2. Analyze, code, and demonstrate the execution of hash table algorithms.
3. Implement and use Maps.
4. Design, code, analyze, and trace recursive algorithms and data structures.
5. Analyze, code, and demonstrate the execution of binary tree and heap algorithms.
---
# Administrivia

# Course Outcomes

1. Analyze, code, and demonstrate the execution of graph algorithms.
2. Analyze and demonstrate the execution of balanced search tree algorithms.
3. Analyze, compare, contrast, and demonstrate the execution of advanced sorting algorithms.
---
# Administrivia

# Course Outcomes

1. Recognize and apply the design patterns of Adapter, Singleton, Visitor, Composite, and Iterator in object-oriented designs.
2. Select and use an appropriate data structure to solve a given problem.
---
# Administrivia

# Academic integrity

- Code on the Web that can serve as “inspiration” for your solutions if:
- You understand the solution as if you had written it yourself.
- You cite your source of inspiration.
- Not citing your source can get you charged with cheating/plagiarism.
---
# Administrivia

# Academic integrity

- Other students cannot serve as a source for your code!
- The closer you move toward sharing code with soliciting code from another person (student or not), the more likely it is that you are cheating.
---
# Administrivia

|Behavior|Danger Level|
|---|---|
|Discussing the concepts of the class/assignments| |
|E-mailing a partial source code solution to another student| |
|E-mailing a link used as “inspiration” to another student| |
|Telling someone about an exam you took before them| |
|Discussing algorithms that will help with assignments| |
|Sharing insights about corner cases in testing| |
|Putting assignments up for bid on rentacoder.com| |
|Copying and pasting another person’s source code| |
|Sharing pseudo-code solutions| |
|Posting help requests for your assignment on a| |
---
# Administrivia

|Behavior|Danger Level|
|---|---|
|Discussing the concepts of the class/assignments| |
|E-mailing a partial source code solution to another student| |
|E-mailing a link used as “inspiration” to another student| |
|Telling someone about an exam you took before them| |
|Discussing algorithms that will help with assignments| |
|Sharing insights about corner cases in testing| |
|Putting assignments up for bid on rentacoder.com| |
|Copying and pasting another person’s source code| |
|Sharing pseudo-code solutions| |
|Posting help requests for your assignment on a| |
---
# Administrivia

# Academic integrity

- If you have a vague feeling that you wouldn’t want your instructor to know about what you’re doing… don’t do it.
- When in doubt, ask your instructor.
---
# Administrivia

# Points breakdown

|Pct|Type|Count|Each|Total|
|---|---|---|---|---|
|25%|Homework|10|25|250|
|35%|Project|10|35|350|
|35%|Exams|2|200|400|
|Total|Total|Total|Total|1000|
---
# Late Submission Penalty

- 1 day late – 10%
- 2 days late – 20%
- 3 days late – 30%
- &gt;3 days late – no credit
---
# Daily/weekly Activities

- Daily: Check discussions
- Before class
1. Read the associated sections from the textbook.
2. Read and consider the weekly homework problems and project work.
- After class
1. Complete the homework assignment
2. Complete the weekly project work
---
# Discussions

- Ask lots of questions
- Consider other students’ posts
- Required reading
- Public, Private and Anonymous Questions
- Hints rather than solutions
- Don’t get discouraged, keep asking
- Office Hours
---
# Debugging

The hard part of programming is not coding, but problem solving

1. You have a test failure in edstem
2. Reproduce with a unit test
3. Debug the problem
- Come up with a clear picture of exactly what you wanted the code to do
- Watch what it actually does in the debugger, and find the difference
---
# The Road Ahead

# Where are we now?

- Writing code to fill in existing methods and classes
- Refactoring methods into base classes
- Relying on edstem to point out problems
- Using println() to debug?
- Solving problems on edstem by guessing?
---
# The Road Ahead

- Where do we want to be?
- Writing new methods
- Writing new classes
- Using the debugger to find problems
- Starting from a blank page
- Working without instructor tests
---
# Homework

- Homework
- Done in edstem
- Reflection problem must be 2-3 paragraphs, and must include at least one question
- Project
- Done in Eclipse? Submitted in edstem
- GitHub required – give me your username
---
# Major Themes

- Design patterns
- Test-driven development
- Recursion
- Non-linear data structures
- Algorithmic efficiency
- Application of patterns and data structures to problem solving
---
# Outcomes

- Recognize and apply the Adapter design pattern to solve a given problem.
- List the common operations and properties of sets.
- How to use Eclipse, GitHub, and edstem.
---
# Adapter Pattern

Speaks

“RCA”

Speaks 1/8 inch
---
# Adapter Pattern

Adapts RCA to 1/8 inch
---
# Adapter Pattern

# ClientClass

Uses

# PotentialTarget

Can’t plug this in to the

# ConcreteTarget
---
# Adapter Pattern

# ClientClass

Uses PotentialTarget Can’t plug this in to the ConcreteTarget

First step: separate interface from implementation
---
# Adapter Pattern

|ClientClass|Uses|interface|
|---|---|---|
|TargetInterface|PotentialTarget|ConcreteTarget|
|Concrete PotentialTarget| | |
---
# Adapter Pattern

|ClientClass|Uses|<<interface>>|<<interface>>|
|---|---|---|---|
|TargetInterface|PotentialTarget|ConcreteTarget|Concrete|
|Client is now|Client is now|Still can’t plug this in to the client|Still can’t plug this in to the client|
---
# Adapter Pattern

ClientClass Uses &lt;&lt;interface&gt;&gt; &lt;&lt;interface&gt;&gt;

TargetInterface PotentialTarget

ConcreteTarget Concrete PotentialTarget

Option 1: implement the TargetInterface.
---
# Adapter Pattern

# Option 1

- Pros: simplest thing that could possibly work.
- Cons:
- Proliferation of “implementations”
- Not reusable – what if there are many ConcretePotentialTargets?
---
# Adapter Pattern

- Option 1
- Pros: simplest thing that could possibly work.
- Cons:
- Proliferation of “implementations”
- Not reusable – what if there are many ConcretePotentialTargets?
- Option 2: Adapt!
---
# Adapter Pattern

|ClientClass|Uses|&lt;&lt;interface&gt;&gt;|
|---|---|---|
|ConcreteTarget|PotentialTargetTo|&lt;&lt;interface&gt;&gt;|
|TargetAdapter|PotentialTarget|Concrete|
| | |ConcretePotentialTarget2|
---
# Adapter Pattern

# The interpreter

|ClientClass|Uses|&lt;&lt;interface&gt;&gt;|between Client|
|---|---|---|---|
| |TargetInterface| |and|
|ConcreteTarget|PotentialTargetTo|&lt;&lt;interface&gt;&gt;|PotentialTarget|
| |TargetAdapter|Concrete|Concrete|
| |PotentialTarget|PotentialTarget2| |
---
# Adapter Pattern

# Option 2

# Pros:

- Reusable solution
- Loose coupling, high cohesion

# Cons:

- More layers of indirection
---
# Learning Activities

- Q: Write an Account to BankAccount adapter.
---
# Learning Activities

- A: We need to use an adapter to use an Account object with code that expects a BankAccount object.
- Implement the BankAccount interface and “forward” the method calls into the underlying Account implementation.
---
# Learning Activities

public interface BankAccount {
void setPin(int pin);
int getPin();
void setOwner(Customer owner);
Customer getOwner();
void setAccountId(int accountId);
int getAccountId();
boolean deposit(Money amount);
boolean withdraw(Money amount);
Money getBalance();
}
---
# Learning Activities

public interface BankAccount {
void setPin(int pin);
int getPin();
void setOwner(Customer owner);
Customer getOwner();
void setAccountId(int accountId);
int getAccountId();
boolean deposit(Money amount);
boolean withdraw(Money amount);
Money getBalance();
}

public interface Account {
void setPin(int pin);
int getPin();
void setOwner(String owner);
String getOwner();
void setAccountId(int accountId);
int getAccountId();
boolean deposit(double amount);
boolean withdraw(double amount);
double getBalance();
}
---
# Learning Activities

|SecondBank|Uses|&lt;&lt;interface&gt;&gt;|
|---|---|---|
|BankAccount| | |
|SimpleBank|AccountToBank|&lt;&lt;interface&gt;&gt;|
|Account|AccountAdapter|Account|
| |SimpleAccount| |
---
# Learning Activities

public class AccountToBankAccountAdapter
implements BankAccount {
private Account parent;
public AccountToBankAccountAdapter(Account a) {
parent = a;
}
public void setPin(int pin) {
parent.setPin(pin);
}
public int getPin() {
return parent.getPin();
}
// setAccountId and getAccountId are
similar...
---
# Learning Activities

public class AccountToBankAccountAdapter
implements BankAccount   {
// continued...
public void setOwner(Customer owner) {
StringBuffer  buf =  new StringBuffer();
buf.append(owner.getFirstName());
buf.append("  ");
buf.append(owner.getLastName());
}   parent.setOwner(buf.toString());
// ...
---
# Learning Activities

public class AccountToBankAccountAdapter
implements BankAccount {
// continued...
public Customer getOwner() {
Customer c = new BankCustomer();
String [] tok = parent.getOwner().split(“);
c.setFirstName(tok[0]);
c.setLastName(tok[1]);
c.setId("" + parent.getAccountId());
}
return c;
}
---
# Learning Activities

public class AccountToBankAccountAdapter
implements BankAccount {
// continued...
public boolean deposit(Money amount) {
}   return parent.deposit(amount.asDouble());
public boolean withdraw(Money amount) {
}   return parent.withdraw(amount.asDouble());
public  Money getBalance() {
}   return new Dollar(parent.getBalance());
}   // end  class
---
# Set Interface

- Holds collection of objects
- Main operations are add, remove, contains, intersection, union
- No duplicates allowed
---
# Learning Activities

• Q: Explain the effects of this code:

Set&lt;String&gt; s  =  new HashSet&lt;String&gt;();
s.add(&quot;hello&quot;);
s.add(&quot;bye&quot;);
s.addAll(s);
Set&lt;String&gt; t  =  new TreeSet&lt;String&gt;();
t.add(&quot;123&quot;);
s.addAll(t);
System.out.println( s.containsAll(t)  );
System.out.println( t.containsAll(s)  );
System.out.println( s.contains(&quot;ace&quot;)  );
System.out.println( s.contains(&quot;123&quot;)  );
s.retainAll(t);
System.out.println( s.contains(&quot;123&quot;)  );
t.retainAll(s);
System.out.println( t.contains(&quot;123&quot;)  );
---
# Learning Activities

A:
Set&lt;String&gt; s =  new HashSet&lt;String&gt;();
// Creates a HashSet  that can hold Strings
s.add(&quot;hello&quot;);
//  Add &ldquo;hello&rdquo;  to  the HashSet
s.add(&quot;bye&quot;);
//  Add &ldquo;hello&rdquo;  to  the HashSet
s.addAll(s);
//  Add all elements of s to the set.  Has no
//  effect,
//  since Sets cannot hold duplicate values.
---
# Learning Activities

Set&lt;String&gt; t = new TreeSet&lt;String&gt;();
// Creates a TreeSet that can hold Strings
t.add(&quot;123&quot;);
// Adds &quot;123&quot; to the TreeSet
s.addAll(t);
// Adds everything from the TreeSet into the HashSet
System.out.println( s.containsAll(t) );
// Prints true
System.out.println( t.containsAll(s) );
// Prints false
---
# Learning Activities

• A:
System.out.println( s.contains("ace")  );
// Prints   false
System.out.println( s.contains("123")  );
// Prints   true
s.retainAll(t);
//  Keeps  only those items in the HashSet that
also
//  exist  in the TreeSet
System.out.println( s.contains("123")  );
// Prints  true
---
# Learning Activities

• A:

t.retainAll(s);
// No effect.  Already the same.
System.out.println( t.contains("123") );
// Prints true
---
# Learning Activities

- Q: List the available Set methods, their purposes, and their efficiencies. Give brief explanations to support your answers.
---
# Learning Activities

A: The methods are the same as in Collection. The semantics are different in that no duplicates are permitted.

public interface Set&lt;E&gt; extends Collection&lt;E&gt; {
// A marker interface only
}
---
# Learning Activities

A: Efficiencies of methods are dependent on the implementation. Most methods in HashSet are O(1) whereas most methods in TreeSet are O(log n).
---
# Tools

- GitHub
- Eclipse
- edstem IDE
---
# Homework 1

- Write a simple adapter class to translate between these two interfaces
- Two methods for printing lists are given along with two claims. Justify the claims.
---
# Homework 1

- Why doesn’t using your own class with HashSet work?
- Meet session reflection
---
# Git Project

# Part 1 Introduction
---
Question and Answer Session
