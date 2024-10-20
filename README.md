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

Following Rust's almost philosophy of assigning everything to the stack, Thrust with strings does the same as C with its fixed arrays but Thrush transforms a string into an array of ascii characters that resizes it at runtime if necessary, for example concatenating strings What Thrush does is take the strings that are going to be concatenated, obtains their size, and calculates how much it should allocate in memory, allocates in the heap memory that part that it needs to then move it to the stack and build the completely already assigned string in the stack.

  
