---
title: "Linkers, do they do things, what do they do, lets find out"
date: 2020-06-26T21:12:56-05:00
draft: true
description: "Linkers: the most important yet under appreciated part of compiling"
categories: "Programming"
tags: ["Compilers", "C++"]
---

If you write C or C++ chances are you've used a makefile a time or two and there is always a rule to take all the object files and combine them into the final executable. usually something along the lines of `gcc -o output foo1.o foo2.o foo3.o`. To answer what that's doing we have to back up to what an object file is and how it is made.

To understand what an object file is lets first talk about compilers. To compile a file you'd run a command like `gcc -c foo1.c` and that would produce a `.o` file or an object file. C and C++ are compiled with whats called a single pass compiler and this is what drives both the need for header files and the need for object files and linking. In the compiler there are a few distinct steps. First the preprocessor is run to produce the real source file. If you're unfamiliar with C or C++ the preprocessor basically does fill in the blank with your source files. For example

{{< highlight c >}}
#define PI 3.14159

//SOME CODE
auto area = PI * r * r;
//MORE CODE
{{< /highlight >}}

would preprocess into 

{{< highlight c >}}
//SOME CODE
auto area = 3.14159 * r * r;
//MORE CODE
{{< /highlight >}}

I will hopefully have a blog post about the preprocessor and compiler coming "soon".

Once the preprocessor is run and the final source file is made. The lexer and parser will come in and break the source file apart. The lexer will get tokens or lexemes from the source file like a variable name or an operator or anything that can be defined with regex and give them to the parser. The parser will then use those lexemes to build whats called an abstract syntax tree. What that is isn't important right now but if you care to learn more that should also be in the parser and compiler blog post. Eventually the parser will come across a symbol, a function or variable name. 

For right now lets look at a simple code example. 

`foobar.c`  
{{<highlight c>}}
//from included file "foobar.h"
//some code
extern int foo;
int bar(int);
//more code
//end file "foobar.h"

//even more code
int foo = 10;
int bar(int wat){
    return wat;
}
//the rest of the code
{{</highlight>}}

`barfoo.c`  
{{<highlight c>}}
//from included file "foobar.h"
//some code
extern int foo;
int bar(int);
//more code
//end file "foobar.h"

//code
int whatever(){
    return foo + bar(foo);
}
//code
{{</highlight>}}

These symbols are the reason for linking and headers. 