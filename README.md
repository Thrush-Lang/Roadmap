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

**Thrush**has full access to the C ABI by default, all extra implementations that are not in C are done directly in the IR, without using the C++ standard library for example, to know concisely what is happening and why it does not work. This also allows us to create our own system directly in IR, instead of using other language libraries. 
On the other hand, **Thrush** tries to be a high-level language, with little memory management by the user. In populist terms a Rust but it is not a concise systems language.

<h1 align="center">The Tecniques</h1>
