# \# Prototype Design Pattern (Java)

# 

# \## Overview

# 

# The \*\*Prototype Design Pattern\*\* is a \*\*creational design pattern\*\* used to create new objects by \*\*cloning an existing instance\*\*, rather than creating them from scratch.

# 

# This approach is especially useful when object creation is costly or complex.

# 

# ---

# 

# \## When to Use Prototype Pattern

# 

# Use this pattern when:

# 

# \- Object creation is \*\*expensive\*\*

# &nbsp; (e.g., database calls, heavy initialization, complex setup)

# \- You need \*\*multiple objects with similar state\*\*

# \- You want to \*\*avoid complex construction logic\*\*

# \- You want to create objects at runtime without tight coupling to constructors

# 

# ---

# 

# \## Core Idea

# 

# Create new objects by \*\*cloning a prototype instance\*\*.

# 

# \### Instead of:

# ```java

# new Object();

# ```

# 

# \### You do:

# ```java

# existingObject.clone();

# ```

# 

# The client does \*\*not\*\* create objects directly using `new`.

# 

# ---

# 

# \## Advantages

# 

# \- Faster object creation

# \- Reduced construction complexity

# \- Dynamic runtime behavior

# \- Better encapsulation of object creation logic

# 

# ---

# 

# \## Important Note About Cloning

# 

# The Prototype pattern \*\*does not require\*\*:

# 

# \- Using `Object.clone()`

# \- Copying raw memory

# \- Implementing `Cloneable`

# 

# A custom `clone()` method that copies the object state is \*\*perfectly valid\*\*.

# 

# ---

# 

# \## Example: Custom Clone Method

# 

# ```java

# @Override

# public Employee clone() {

# &nbsp;   return new Employee(this.name, this.department);

# }

# ```

# 

# ✔ This is valid prototype cloning because:

# \- It creates a \*\*new object\*\*

# \- The new object has the \*\*same state\*\*

# \- The client \*\*does not use `new` directly\*\*

# \- Object creation logic is encapsulated

# 

# ---

# 

# \## Example Usage

# 

# ```java

# Employee original = new Employee("Piyum", "Engineering");

# 

# Employee clone1 = original.clone();

# clone1.setName("Kamal");

# 

# Employee clone2 = original.clone();

# clone2.setName("Nimal");

# ```

# 

# ---

# 

# \## Summary

# 

# Prototype Pattern allows object creation by duplicating an existing object's state, making it ideal for scenarios where many similar objects are required and creation cost is high.



