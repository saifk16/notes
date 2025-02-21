ok# GSoC 2025

  Gsoc 2025 is here... read => [blog-1](https://opensource.googleblog.com/2025/01/google-summer-of-code-2025-is-here.html)

## 1. 20 years of GSoC

started in 2005... read => [blog-2]()

## 2. What is Google Summer of Code?

Google Summer of Code is a global, online program focused on bringing new contributors into open source software development. GSoC Contributors work with an open source organization on a 12+ week programming project under the guidance of mentors.

## 3. Organisations

#### Haskell

Haskell, ghc

## 4. Projects
#### Qualified aliases in Liquid Haskell

##### Goals
Update the implementation of Liquid Haskell to allow referring to type and predicate aliases in qualified form.

##### Background
Liquid Haskell is a verification tool for Haskell programs. The programmer writes specifications for these programs, and Liquid Haskell checks if the programs actually meet the specifications.

Recently, the Liquid Haskell implementation went through a refactoring to improve name resolution. Much of the names in the specification language can be qualified now, in order to dissambiguate equal names that come from different modules. There is an exception though, when it comes to type and predicate aliases. For technical reasons, this constructs have been left behind in the refactoring.

As the reference documentation explains, type aliases can be used to shorten specifications. Instead of writing a spec like:

```haskell

{-@ length :: [a] -> {v:Int | v >= 0} @-}

```

one can write

```haskell

{-@ type INat = {v:Int | v >= 0} @-}

{-@ length :: [a] -> INat @-}

```

Unfortunately, if there are multiple INat aliases in scope, Liquid Haskell does not allow to qualify the name to disambiguate. For instance, the following specification is rejected with a message that says that SomeImport.INat is not in scope.

```haskell

{-@ length :: [a] -> SomeImport.INat @-}

```

This project is to analyze the implementation and to design and implement a solution both for type and predicate aliases. There is a corresponding issue in the Liquid Haskell repo.

##### Outcomes
The main outcomes are a pull request with the implementation, tests, and code documentation, and a discussion of the analysis and the design in the corresponding issue. A secondary outcome is a blogpost describing the experience and the results of the project.

##### Size
Project size should be near 175 hours. The project will require a fair amount of reading of existing Haskell code, and building an understanding of how it works. Familiarity with the verification mechanisms is not necessary a priori, though some user-level understanding of Liquid Haskell is going to be needed to write tests.

##### Required Skills
- Read and write technical English
- Haskell programming basics

##### Project Mentor
Facundo Domínguez, Tweag engineer and comaintainer of Liquid Haskell