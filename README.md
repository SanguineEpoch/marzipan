# Marzipan

**Please Note:** Marzipan is currently in its design stage. This means that the features, syntax, and information available in this repository are experimental and subject to significant changes. **The claims about Marzipan below describe it's current aspirations, rather than its current state.**

## Introduction

Marzipan is a high-level, general-purpose programming language designed to be both powerful and delightful to use. Its hybrid paradigm approach allows developers the freedom to choose programming styles best suited to their tasks. Marzipan's unique execution strategy, Progressive Adaptive Layered Execution (PALE), offers the flexibility of interpreted languages while delivering performance that approaches that of compiled languages. Marzipan's robust configuration system allows you to tweak Marzipan's execution strategies suited best for your environment (and much more.) Its type system is adaptable enough for rapid prototyping yet robust enough to build reliable systems you can depend on.

## Progressive Adaptive Layered Execution (PALE)

Marzipan employs a sophisticated execution model called Progressive Adaptive Layered Execution (PALE), which combines the flexibility of interpreted languages with the performance benefits of compiled languages. Below is an overview of the components of PALE:

- **Progressive**: Marzipan programs optimize progressively, improving performance over time, until it is optimized to its limit.
- **Adaptive**: The optimization strategy is not static but adapts based on runtime conditions, heuristics, user defined configuration, and other metrics, ensuring optimal performance tailored to the application’s needs.
- **Layered**: This refers to the tiered approach Marzipan takes toward executing code. Each layer represents a different execution strategy, ranging from direct interpretation to full machine code compilation:
  - **Interpreted**: The highest layer, where code is executed directly without compilation.
  - **Pseudo Layer**: Includes optimizations at the AST level.
  - **LLVM IR**: Intermediate representation that may be compiled to machine code directly or be optimized.
  - **Machine Code**: The lowest layer, representing fully compiled code via LLVM IR.
- **Execution**: The term underscores that Marzipan's model does not fit neatly into traditional categories of compiled or interpreted languages due to its dynamic and flexible nature.

## Key Features of PALE

- **Configurable Execution Strategies**: Users can tailor Marzipan’s execution strategy to fit their specific needs, whether prioritizing lower latency through direct interpretation or maximizing performance via compilation/optimization strategies of varying intensity. This makes Marzipan highly adaptable, capable of optimizing specific operations like matrix multiplication, and versatile enough to meet various performance and operational requirements. **Marzipan can act like interpreted, compiled, and anywhere in between.**

- **AST Manipulation for Metaprogramming**: In the future, Marzipan will support runtime AST (Abstract Syntax Tree) manipulations that can dynamically reflect onto the codebase. In other words Marzipan will allow for programs to change their own code during runtime. PALE will be able to progressively optimize new changes, meaning long term performance isn't sacrificed. This feature will be **opt-in**, accommodating the additional performance requirements it entails. Once implemented, this will be particularly beneficial for developing systems, such as AI models that can improve and extend their own codebase in real-time. This powerful metaprogramming feature is targeted for inclusion once Marzipan matures. This is definitely an ambitious feature, however if idealized well, Marzipan will offer unprecedented flexibility.

#### Benefits

PALE ensures that Marzipan remains both performant and flexible, capable of adapting to diverse runtime environments and user needs. It allows for developers to configure Marzipan to be suited best for its needs, as well as allows the possibility of future real-time, efficient AST manipulation without sacrificing the potential for long-term performance optimization, embodying a truly modular and adaptive approach to programming language design.

## Programming Paradigm

Marzipan is designed as a multi-paradigm programming language, seamlessly integrating procedural, object-oriented, and functional programming styles. While Marzipan supports the flexibility for developers to adopt the paradigm that best suits their needs or preferences, it encourages a hybrid approach. The Marzipan "way" emphasizes leveraging the strengths of both object-oriented and functional paradigms to achieve optimal maintainability and efficiency in software. This approach allows developers to utilize the right tools for specific tasks, promoting clean, scalable, and robust code across various use cases.

## Type System

Marzipan's type system combines the ease of dynamic typing with the precision of optional type annotations. Here’s a quick overview:

- **Dynamic Typing**: Marzipan is dynamically typed, allowing for quick coding and prototyping. You can focus more on developing features without getting bogged down by strict type definitions from the start.

- **Optional Type Annotations**: While Marzipan thrives on flexibility, you have the option to use type annotations to make your code clearer and more maintainable. This is especially useful in larger projects where specifying types can prevent bugs and aid in optimization.

- **Strong Type Inference**: Even without explicit type annotations, Marzipan is smart enough to figure out what type your variables should be. This keeps your code clean and efficient, providing the best of both worlds—type safety without the verbosity.

- **Generics Support**: Marzipan will support generics, allowing you to write adaptable and reusable code that doesn’t compromise on type safety. This will make it easier to handle diverse data types and design flexible systems.

#### Benefits

Marzipan's type system is designed to be as flexible or as strict as you need it to be, supporting everything from rapid scripting to the development of complex, large-scale applications.

## Conclusion

Programming in Marzipan is designed to be as delightful and straightforward as its namesake suggests. Its syntax is designed to be both simple and powerful, supporting rapid prototyping and robust application development without sacrificing performance. Marzipan aims to make programming a sweet experience, optimizing both the process and the outcomes for developers. Marzipan is a good choice for any software that needs (or wants) long-term performance, runtime flexibility, quick prototyping and/or robust systems, while also providing an enjoyable programming experience.
