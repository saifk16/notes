# GSoC 2025

  Gsoc 2025 is here... read => [blog-1](https://opensource.googleblog.com/2025/01/google-summer-of-code-2025-is-here.html)

## 1. 20 years of GSoC

started in 2005... read => [blog-2]()

## 2. What is Google Summer of Code?

Google Summer of Code is a global, online program focused on bringing new contributors into open source software development. GSoC Contributors work with an open source organization on a 12+ week programming project under the guidance of mentors.

## 3. Organisations

Java path finder

java core java jvm java internals bytecode jvm internals

## 4. Projects

####  Support for Java 17 for jpf-core

[Link](https://github.com/javapathfinder/jpf-core/wiki/GSoC-2025-Project-Ideas#-support-for-java-17-for-jpf-core)

Related to the project above, there are also some new features in Java 17 that are not yet supported by JPF. We have work in progress on branch `java-17`. Currently unsupported Java features include language features that are not supported at run time (e.g., records) and Java language features that are not fully analyzed (e.g., sealed classes). In this project, you would identify such unsupported features and extend JPF (jpf-core) to support them.

**Difficulty:** Medium  
**Scope:** 175 hours  
**Required skills:** Knowledge of Java internals  
**Possible Mentors:** Cyrille

#### Support runtime exception in SPF

[Link](https://github.com/javapathfinder/jpf-core/wiki/GSoC-2025-Project-Ideas#-support-runtime-exception-in-spf)

**Description:** The main goal of this project is to support throwing a runtime exception for some of the summarized functions such as `String.substring`. Also, this project should build on [SPF](https://github.com/SymbolicPathFinder/jpf-symbc) Java 11 Gradle support, which implies fixing existing issues.

**Difficulty:** Meduim  
**Scope:** 175 hours  
**Required skills:** Knowledge of Symbolic Pathfinder  
**Possible Mentors:** Soha