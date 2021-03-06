README

Material for:
Compilers COMP3012, University of Nottingham, 2021
Venanzio Capretta / Nicolai Kraus

During the lab sessions on 20 October, 27 October, and 3 November,
you have worked on a compiler for the language of arithmetic
expressions extended with boolean operations. This archive contains
such a compiler that uses functional parsers.

Contents:

(1) FunParser.hs

This is a library with many useful functions. You can (and are
encouraged to) build on this library for your further work. It
contains the implementations of Parser as a member of the typeclasses
Functor, Applicative, Monad, and Alternative that we have discussed
in the lecture. It also contains many auxiliary functions that you
may find useful for the coursework.

(2) ExpParser.hs

This file builds on the library above. It defines the type of
abstract syntax trees of arithmetic expressions (including boolean
operators) and a parser.

(3) TAM.hs

Defines TAM programs. In addition to what we have done so far, this
file contains a parser for TAM programs, i.e. it allows you to take
a string and read it as a TAM program. This is very easy compared to
parsing arithmetic expressions.

(4) ExpTAM.hs
 
A translation from the abstract syntax trees defined above to TAM,
i.e. a Code Generator.

(5) ExpCompiler.hs

Uses all the modules above to define a compiler.

(6,7) arith_example.exp, arith_example2.exp

Files with sample arithmetic expressions. See below.

(8) Main.hs

Main file. You can use a command such as
  ghc Main -o aec
to produce an executable aec (for "Arith Expression Compiler") that
both compiles files containing arithmetic expressions and executes
TAM code, according to the extension of the file.
This executable can be used on files with two different extensions,
.exp and .tam

Files with ending .exp contain an arithmetic expression, see the
sample files (6,7). If you run aec with such a file, it generates
a file with extension .tam containing the corresponding TAM code.

E.g.: The command
  ./aec arith_example.exp
should generate a file arith_example.tam containing the TAM code
for the expression in the sample file in this directory.

If you run aec with a file with extension .tam, it should execute the
TAM code and print the final result.

E.g.
  ./aec arith_example.tam
should run the code generated by the previous command and print the
result (45).

