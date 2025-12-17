# HAKE Programming Language
## 🌟 Project Overview

HAKE is a new programming language developed purely in C, focusing on simplicity, efficiency, and ease of learning. We believe a programming language should be both simple and powerful, allowing developers to focus on solving problems rather than complex syntax.

Design Philosophy:

🚀 High Performance:​ Compiles directly to native code with no VM overhead.

📚 Easy to Learn:​ Clean syntax for a quick start.

🛠️ Concise Code:​ Intuitive function design, easy to understand and maintain.

💻 Built with C:​ Leverages the efficiency of C to ensure the language's own performance.

## ✨ Core Features

Performance First

Direct Compilation:​ Compiles to efficient native code.

Zero Runtime Overhead:​ No garbage collector; manual memory management (with optional automatic features planned).

Lightweight:​ Core compiler aims to be under 1MB.

Concise Syntax

// Target HAKE syntax example (design goal)
func main() {
    print("Hello, HAKE!")
    let x = 10
    if x > 5 {
        print("x is greater than 5")
    }
}

Easy to Learn

C-like syntax with modern improvements.

Simplified type system.

Clear error messages.

## 🏗️ Project Status

Current Stage:​ Early Development - Contributors are welcome!

## 📊 Development Progress:

[▓▓▓▓▓▓░░░░] 50%- Language Specification Design

[▓▓▓░░░░░░░] 30%- Lexer

[▓▓░░░░░░░░] 20%- Parser

[░░░░░░░░░░] 0%- Code Generator

Note for Contributors:​ The lexer (src/lexer/) currently handles identifiers, integers, and keywords. A great starting point is the lex_next_tokenfunction in src/lexer/lexer.c. The next goal is to add string literal support.

## 🚀 Quick Start

Prerequisites

C Compiler:​ GCC 9.0+ or Clang 10.0+

Build Tools:​ Make or CMake

System:​ Linux, macOS, or Windows (via WSL)

Build the Project

# 1. Clone the repository
git clone https://github.com/xujz66666/HAKE-programming-language.git
cd HAKE-programming-language

# 2. Build the compiler
make build

# 3. Run tests
make test

Your First HAKE Program

Create a file hello.hake:

// A simple HAKE program
func main(): int {
    print("Hello, HAKE World!")
    return 0
}

Compile and run (This is the target workflow):


./hake compile hello.hake
./hello
## 📁 Project Structure
HAKE/
├── src/                 # Source Code
│   ├── lexer/          # Lexer - Concise function design
│   ├── parser/         # Parser - Clear logical structure
│   ├── codegen/        # Code Generator - Efficient C code output
│   └── utils/          # Utility Functions - Reusable components
├── examples/           # Example Code
├── tests/              # Test Suite
└── docs/               # Documentation
## 🎯 Design Principles

Simple and Clear Functions

Each function follows the Single Responsibility Principle, keeping it short (typically <50 lines).

// Example: A clear lexer function
Token* lex_next_token(Lexer* lexer) {
    skip_whitespace(lexer);
    return identify_token(lexer);
}

// Clear error handling
void report_error(const char* msg, int line) {
    fprintf(stderr, "Error at line %d: %s\n", line, msg);
}

Fast Execution

Single-pass compilation strategy.

Minimal memory allocation.

Optimized hash table lookups.

Easy to Learn

Familiar C-like syntax.

Gentle learning curve.

Rich examples and documentation.

## 🤝 How to Contribute

We warmly welcome all contributors, especially C language enthusiasts!

Tasks for Beginners

good-first-issue- Simple function implementations.

documentation- Documentation improvements.

testing- Writing test cases.

Contribution Workflow

Fork this repository.

Create a feature branch: git checkout -b feature/YourFeatureName

Commit your changes: git commit -am 'Add some concise feature'

Push the branch: git push origin feature/YourFeatureName

Open a Pull Request.

Code Standards

Functions should not exceed 50 lines.

Use meaningful variable names.

Provide clear comments.

Each function should have corresponding tests.

## 🗺️ Development Roadmap

v0.1.0 (Current)

[x] Project infrastructure

[ ] Basic Lexer

[ ] Simple Parser

[ ] Code generator that outputs C code

v0.5.0 (Next)

[ ] Complete language features

[ ] Optimized compiler

[ ] Basic standard library

v1.0.0 (Goal)

[ ] Stable language specification

[ ] Production-ready compiler

[ ] Rich ecosystem

## 💬 Community & Communication

GitHub Issues:​ For problem discussions and feature suggestions.

GitHub Discussions:​ For technical exchange and design discussions. (Please ensure this is enabled in your repository settings).

Share Examples:​ Share your HAKE code examples!

## ❓ Frequently Asked Questions (FAQ)

Q: Why was C chosen for development?

A: C is chosen for its high performance and closeness to hardware, making it ideal for building an efficient compiler.

Q: What level of C knowledge is needed to contribute?

A: Basic C knowledge is sufficient! You can start with simple functions and learn progressively.

Q: What are HAKE's advantages compared to other languages?

A: HAKE aims to offer the performance of C with a cleaner syntax and a better development experience.

Q: How can I start learning about compiler development?

A: Start with the src/lexer/directory. Lexical analysis is the most understandable part to begin with.

##  📄 License

This project is licensed under the MIT License - see the LICENSEfile for details.

## 🙏 Acknowledgments

Thanks to all the developers who contribute to the HAKE project! Special thanks to the C language community for its wealth of resources.

Let's build a simple and efficient programming language with C! 🚀

If you find this project helpful, please give us a ⭐️!

"Simplicity is a prerequisite for reliability." - Edsger W. Dijkstra
