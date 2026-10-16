# Tinyjson

Learn C++ by building a small JSON parser, from basic syntax and classes to modern C++ features.

This is a learning project in progress. The code starts with a simple, explicit design and will evolve as new concepts are introduced. The target language standard is **C++20**.

## Current state

The program represents the six JSON value types with an `enum class` and a `Value` struct. It manually constructs the equivalent of:

```json
{
  "name": "tiny",
  "stars": 5,
  "tags": [true, null]
}
```

It then prints the number of object keys and array elements. Parsing JSON text and serializing values back to text are planned; they are not implemented yet.

## Build and run

Use a C++ compiler with C++20 support. From the repository root, with GCC available on your PATH:

**Windows PowerShell**

```powershell
g++ -std=c++20 -Wall -Wextra src/main.cpp -o tinyjson.exe
.\tinyjson.exe
```

**Linux / macOS**

```sh
g++ -std=c++20 -Wall -Wextra src/main.cpp -o tinyjson
./tinyjson
```

Expected output:

```text
root is an object with 3 keys
tags has 2 elements
```

## Learning approach

Teaching takes place in the chat, in both Chinese and English. Each step introduces a small concept, connects it to this project, explains the relevant code, and provides a short exercise before moving on.

The repository contains source code and this project overview. Lesson transcripts are kept in the chat rather than in separate lesson documents. Documentation and code comments use English.

## Learning path

1. **C++ basics**: compilation, `main`, variables, types, functions, conditions, loops, and standard output.
2. **Classes and objects**: `struct` versus `class`, members, access control, constructors, initialization, and encapsulation.
3. **JSON values and containers**: `enum class`, type aliases, forward declarations, `std::string`, `std::vector`, and `std::map`.
4. **References and object lifetime**: `const`, references, value semantics, copying, RAII, and moving.
5. **Parsing**: tokenization, `std::string_view`, literal and string handling, recursive arrays and objects, and useful error messages.
6. **Modern C++ improvements**: C++17 `std::variant`, `std::visit`, `std::optional`, structured bindings, and `std::from_chars`; C++20 concepts and `requires`.
7. **Completing the parser**: serialization, focused tests, edge cases, and clearer interfaces.

These are learning goals, not a list of completed features. Features will be introduced when they solve a problem in the code.

## Repository layout

```text
Tinyjson/
|-- src/
|   `-- main.cpp    # Current data model and demonstration
|-- README.md
`-- LICENSE
```

## License

[MIT](LICENSE)
