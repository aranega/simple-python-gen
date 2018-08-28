Very Simple UML to Python Generator
===================================

Very simple Accelo Python generator from UML class diagram. This generator is presented as an example and can be used as work basis but, depending on your purpose, is definitively not enough.

## Sources ##
Model to text (m2t) source is located in `simple-python/codegen` folder while generator is described by `simple-python/generator.xml` file.

## UML Diagram & Translation ##
Class diagrams contained in an UML project are used for python code generation. Python compilation choices are reported in the following table.

| UML | Python  |
| :-: |:-------:|
| Package | module file|
| Class | class |
| Abstract Class | abstract class |
| DataType | class |
| Interface | class |
| Property | class attribute |
| Abstract Operation | abstract operation |
| Class Operation | class operation |
| Operation | instance method |
| Enumeration | class |
| Function Behavior | implementation of operation |
| Class Constructor | definition of `__init__` method |
| Generalization | corresponding `import` statement |
| Use (any Dependency) | corresponding `import` statement |
| Instance Specification | Named instanciation without any further initialization |

## Comments ##
- The generated `import` and inheritance statements are [sorted](simple-python/codegen/uml2python.mtl#23) to avoid unintended differences during source code generation. This might interfere with Python's MRO.
- Function Behavior language needs to be `Python` to be included
- User Code areas are located to alter the respective behavior in the most flexible ways
