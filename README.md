<p align="center">
  <img src= "https://github.com/Thrush-Lang/.github/blob/main/assets/Thrush.png" alt= "logo" style= "width: 2hv; height: 2hv;"> </img>
</p>

<h1 align="center">Roadmap</h1> 

**Thrush Programming Language** tries to be a high-level language but with the characteristic of being memory safe and with a concise and easy to understand syntax. Follow Rust's method of hosting as much as possible on the Stack instead of the Heap. Only in certain areas where it is necessary to use the heap will you have to use the heap. This creates a memory leak-free and fast program. Thrush also tends to form all functions intrinsically and directly in the IR rather than making abstractions in the language itself, which provides concise language development at the last frontier that the compiler touches.

<h1 align="center">The Core</h1>

<p align="center">First let's start with Thrush compiling to LLVM Intermediate Representation by default.</p> 

<p align="center">
  <img src= "https://github.com/Thrush-Lang/Roadmap/blob/master/assets/llvm.png" alt= "llvm" style= "width: 1hv; height: 1hv;"> </img>
</p>

**Thrush** has full access to the C ABI by default, all extra implementations that are not in C are done directly in the IR, without using the C++ standard library for example, to know concisely what is happening and why it does not work. This also allows us to create our own system directly in IR, instead of using other language libraries. 
On the other hand, **Thrush** tries to be a high-level language, with little memory management by the user. In populist terms a Rust but it is not a concise systems language.

<h1 align="center">The Roadmap</h1>

- Implement error handling similar to Rust or Try Catch in other languages. 

- Implement the definition of errors as in Rust.

- Try to have a standard library that offers everything an average developer needs. 

- An asynchronous motor for functions.

- Implement partial object-oriented programming to the extent possible.

- Focus the language more on the functional paradigm.

- And the rest of the capabilities of a current modern language such as V lang, Rust, Zig, but without being directly a language for systems development, more like Kotlin with syntax not so much like JVM languages. And it emits binaries by default.

<h1 align="center">The Currently Tecniques</h1>

<h3 align="center">The String Infraestructure</h1>

The internal string infrastructure in Thrush, by default, uses the creation of a vector system full of ascii characters in the LLVM IR directly, to resolve string return in functions and create a memory-safe environment, as well as being much more dynamic, something equivalent to the string type in Rust, but not the &str type. Of course it allocates to the heap, which perhaps causes a little more slowdown in the program but is compensated by the capabilities and flexibility provided by this internal API.

```
fn main() {

  var hello: string = "Hello!";
  // ^^^^^^^^^^^^^^^^^^^^^^^^^
  // string var = Vec<u8> assigned directly to heap

}
```

Of course this does not happen in all cases, since if it is not a variable or modification such as string concatenation, the compiler takes the string and transforms it into a constant assigned to the stack.

```
fn main() {

  println("%s", "hello");
  //      ^^^^  ^^^^^^^
  // Equivalent to &str type in Rust, assigned to the stack automatically.

}
```



  
