# spi
The usage of the Service Provider Interface in Java is a great way to make your program more extensible.
However, implementing and distributing such an Interface is error prone.

One of the reasons is that the system depends on naming schemes and text files. The name of an implementation
should be put in a text file, located on the classpath in a folder called META-INF/services/<qualified interface name>.

This project allows the programmer to use an Annotation, @ProviderFor, to flag a class as an implementation of
a certain interface. During compilation, the necessary files are created at the appropriate locations. Also, the
class is inspected to see if it follows all rules applicable to Service Providers. Compile time errors will be generated
if those rules are broken, assisting the programmer to create more robust code.

