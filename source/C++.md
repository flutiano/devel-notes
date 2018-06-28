C++/C Study Notes
=================

Tips
----
1. How to compile a .cpp file to assembly in intel syntax:   
    g++ -S -masm=intel file.cpp
	
Books
-----
1. *C++ Primer, 5th Ed*
2. C++ Primer Plus, 6th Ed.
3. C Primer Plus, 6th Ed.
4. Programming: Principles and Practice, Stroustrup, 2e, 2014
5. Learn C++ Programming Language: Become A Complete Programmer
6. C++ Programming Language, Stroustrup, 4e
- Modern C++ Design: Generic Programming and Design Patterns Applied, By Andrei Alexandrescu, AW, 2001, p352
- *The C++ Programming Language, 4th Ed., Bjarne Stroustrup, 2013, p1366*
- Professional C++, MARC GREGOIRE, 3rd Ed., 2014, 987p
- C++ Strategies and Tactics, AWS, 199x
- Programming Abstractions in C++, 682p
- C++ for Mathematicians, An Introduction for Students and Professionals, 2006, 521p
  * We approach C++ from the point of view of solving mathematical problems. 
  * We organize our discussion around the mathematics and bring in the relevant C++ ideas as we need them
- Advanced C Topics, 2011, 304p
- C++ Design Pattern and Derivatives Pricing, 2008
- An Introduction to Design Patterns in C++ with Qt4, 2nd Ed., 2012, 766p
- Advanced C, 1992, 802p
- C in Nutshell
- 21st Century C	

Toolchains
----------

### Microsoft Toolchains
1. Setting the Path and Environment Variables for Command-Line Builds: http://msdn.microsoft.com/en-us/library/f2ccy3wt.aspx

### C++11 Compliance Compilers
1. Visual Studio 2015 
2. GCC 4.9 ( g++ --std=c++11 ... )
3. Clang/LLVM 3.5  ( on Windows with VS2013 build: clang-cl /GR- /D_HAS_EXCEPTIONS=0 ... )

Pre-defined Compiler Macros: http://sourceforge.net/p/predef/wiki/Compilers/
