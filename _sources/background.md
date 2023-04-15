# Compiled Language

A compiled language uses a compiler to translate source code to machine code (a.k.a. a binary executable file). The compiler reads the entire source code project to create an executable file specific to a particular hardware architecture. Examples of compiled languages are C, C++, and Fortran.

![compiled language image](/images/CompiledLanguage.png)

# Interpreted Language

An interpreted language uses an interpreter to translate source code to machine code. The interpreter reads the source code line by line at runtime, and produces machine code on the fly. Examples of interpreted languages are Python, Javascript, and Ruby.

![interpreted language image](/images/InterpretedLanguage.png)

# Hybrid using Just In Time Compilation

Just in time (JIT) uses an interpreter to produce compiled code at runtime, and is a hybrid between a compiled language and an interpreted language. The first time the code is run may execute slowly, but subsequent runs will utilize the compiled machine code and will execute quickly.

![JIT image](/images/HybridJIT.png)

# Pros and Cons

|                  | Compiled | Interpreted | JIT |
| ---------------- | -------- | ----------- | --- |
| Execution Speed  | ✔️       | ✖️         | ✅  |
| Code Development | ✖️       | ✔️         | ✔️  |
| Private Code     | ✔️       | ✖️         | ✖️  |
| Portability      | ✖️       | ✔️         | ✔️  |
