# Uncommon Ruby Bug: Modifying Instance Variables via Getter Methods

This repository demonstrates a subtle bug in Ruby related to modifying instance variables through getter methods.  The code attempts to modify the `@value` instance variable using the `value` getter method. However, this approach will not work as the getter method only returns the value of the instance variable; it does not provide a setter mechanism.

**Understanding the Problem**

In Ruby, getter methods are primarily for accessing the value of instance variables, not for modifying them.  Directly attempting to assign a new value to a getter method won't modify the internal state of the object.

**Solution**

To modify the instance variable, you need to explicitly define a setter method (e.g., `value=`) or use the `attr_accessor` macro.
