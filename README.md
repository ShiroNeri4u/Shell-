# Shell-
A Simple Shell Script Extension.
Testing in Android shell environment, can be used in sh/bash/zsh/fish.

## Usage
``` shell
# Initialization script
source toolkit
InitToolkit

# Defind class
@DefClass ExampleClass

 # Defind attribute

 @DefAttribute ExampleAttribute

 # Defind method
 @DefMethod PrintMethodName
 ExampleClass::PrintMethodName() {
 echo "The Attribute is $This_ExampleAttribute."
 }

 # The constructor function
 ExampleClass::ExampleClass() {
 This_ExampleAttribute=$1
 }

# Create a object
 @New ExampleClass ExampleObject hello

# Use object method
 ExampleObject.PrintMethodName

# Defind sub class
 @DefClass AnotherClass : ExampleClass
  @DefAttribute AnotherAttribute
  AnotherClass::AnotherClass() {
  this.ExampleClass $1
  this_AnotherAttribute=$2
  }

  @DefMethod AnotherMethod
  AnotherClass::AnotherMethod() {
  echo "$this_ExampleAttribute $this_AnotherAttribute"
  }

 @New AnotherClass AnotherObject hello world!

# Type of object

 @Typeof ExampleObject

# Object instance id

 echo $ExampleObject

# Destory object
 @Destory ExampleObject
 @Destory AnotherObject

```