# Compiled Languages, Interpreted Languages, and JIT

To understand why execution speed is slower in Python than many other languages requires some background knowledge of compilers vs. interpreters, and compiled languages vs. interpreted languages. This section provides some background information.

## Compiled Language

A compiled language uses a compiler to translate source code to machine code (a.k.a. a binary executable file). The compiler reads the entire source code project to create an executable file specific to a particular hardware architecture. Examples of compiled languages are C, C++, and Fortran.

![compiled language image](/images/CompiledLanguage.png)
*Figure 1. Schematic of compiled language operations.*

## Interpreted Language

An interpreted language uses an interpreter to translate source code to machine code. The interpreter reads the source code line by line at runtime, and produces machine code on the fly. Examples of interpreted languages are Python, Javascript, and Ruby.

![interpreted language image](/images/InterpretedLanguage.png)
*Figure 2. Schematic of interpreted language operations.*

## Hybrid using Just In Time Compilation

Just in time (JIT) uses an interpreter to produce compiled code at runtime, and is a hybrid between a compiled language and an interpreted language. The first time the code is run may execute slowly, but subsequent runs will utilize the compiled machine code and will execute quickly.

![JIT image](/images/HybridJIT.png)
*Figure 3. Schematic of just-in-time (JIT) compilation.*

## Pros and Cons

Compiled languages have faster execution speed than interpreted languages because the compiler has already created the machine code. Interpeted languages have to perform runtime operations that reduce execution speed. For example, Python must check the type of each variable before a simple addition operation to make sure the types are compatible. If they aren't it returns an error. JIT may exhibit execution speeds comparable to compiled languages, with the caveat that the code must be compiled upon the first execution, which takes some time. Subsequent executions will be faster.

Interpreted languages are often faster for code development because many operations are handled by the interpreter, and need not be written by the code developer. For example, variable types do not need to be declared in Python because the interpeter infers them at rutime. This is very convenient, and allows developers to more rapidly write their code.

Compiled languages allow developers to keep their source code private because they can deploy a binary executable file that users can run on their own computers (assuming hardware compatibility). By contrast, interpreted languages require disclosure of the source code, which must be interpreted every time the code is executed.

Interpreted languages are more portable because the source code is disclosed, and can be interpreted on any user's computer. Compiled binary executables are hardware-specific, and different binary files may be required for different operating systems (e.g., PC vs. Mac vs. Unix).

*Table 1. Pros and cons of compiled, interpreted, and hybrid (JIT).*
|                  | Compiled | Interpreted | JIT |
| ---------------- | :------: | :---------: | :-: |
| Execution Speed  | ✔️       | ✖️         | ✔️* |
| Code Development | ✖️       | ✔️         | ✔️  |
| Private Code     | ✔️       | ✖️         | ✖️  |
| Portability      | ✖️       | ✔️         | ✔️  |
