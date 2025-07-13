# Loge: A C Compiler Written in C

<!--
## The Spark of Creation

Like Loge, the cunning fire god from Wagner's Das Rheingold, I am no traditional compiler craftsman. Yet, driven by the spark of curiosity and a passion for creation, I am forging **Loge**, a compiler for the C programming language written in C. This project is my Valhalla—a monument to the power of personal exploration, built outside the confines of my professional domain.
-->

## Project Overview

Loge is a compiler designed to process a subset of the C programming language, The initial goal is to support a subset of the C language, including basic constructs such as variables, arithmetic operations, conditionals, loops, and functions, with potential expansion to full C standard compliance.


## Objectives
- **Input**: C source code (a subset of ANSI C for the initial version).
- **Output**: Assembly code or intermediate representation (IR) that can be assembled into machine code.
- **Features**:
  - Lexical analysis to tokenize C source code.
  - Syntactic analysis to build an Abstract Syntax Tree (AST).
  - Semantic analysis to check types and scoping rules.
  - Code generation targeting a simple architecture (e.g., x86 or a virtual machine).
- **Self-hosting**: The compiler will be written in C and eventually capable of compiling itself.
- **Modularity**: Designed with clear separation of concerns (lexer, parser, code generator).

## Implementation Plan
1. **Lexer**: Tokenize the input C source code into keywords, identifiers, operators, and literals.
2. **Parser**: Construct an AST based on C grammar rules (using a recursive descent parser for simplicity).
3. **Semantic Analysis**: Validate types, scopes, and other semantic rules.
4. **Code Generation**: Generate assembly code or IR (e.g., LLVM IR for portability).
5. **Optimization** (optional): Implement basic optimizations like constant folding.
6. **Backend**: Link with an assembler or use a virtual machine for execution.

## Tools and Dependencies
- **C Compiler**: GCC or Clang to compile the Loge compiler itself.
- **Flex/Bison** (optional): For generating lexer and parser code, though a hand-written lexer/parser is preferred for learning purposes.
- **Assembler/Linker**: NASM or GAS for x86 assembly, or LLVM for IR-based compilation.
- **Testing Framework**: Custom test suite to validate lexer, parser, and code generation.

## Example Usage
```bash
./loge input.c -o output.asm
```
This command takes a C source file (`input.c`) and generates assembly code (`output.asm`).

## Future Goals
- Support full ANSI C and C99 features.
- Add optimizations for performance.
- Enable self-hosting by compiling Loge with itself.
- Cross-platform support for multiple architectures.
