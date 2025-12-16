# Prototype Pattern



A creational design pattern



When --> 

the object creation is expensive (DB calls, heavy initializations), this pattern is used

if you need more objects with similar state

if you want to avoid complex construction logics





Create new objects by cloning a prototype instance

Instead of:

new Object();

You do:

existingObject.clone();







Advantages 

* Faster object creation
* Dynamic runtime behavior



This doesn't want to use Object.clone() method or copying raw memory or using clonable



@Override

public Employee clone() {

&nbsp;   return new Employee(this.name, this.department);

}



this is perfectly fine for cloning the object

because it also creates a new object, It has a same STATE, The client doesn't want to use <new> directly



&nbsp;       

Example-> 



Employee original = new Employee("Piyum", "Engineering");



&nbsp;       Employee clone1 = original.clone();

&nbsp;       clone1.setName("Kamal");



&nbsp;       Employee clone2 = original.clone();

&nbsp;       clone2.setName("Nimal");





