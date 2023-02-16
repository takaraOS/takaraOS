<div style="align:center">
    <img src="assets/logo.png" style="margin:auto" />
</div>
# TakaraOS
TakaraOS is a microkernel OS written in Rust that can run WebAssembly (Wasm) code at ring 0. This unique capability has the potential to **revolutionize the way we build low-level applications**, allowing developers to write self-contained modules in a variety of programming languages. The result is a highly efficient, secure, and flexible operating system that is ideal for embedded systems and IoT devices.

## TL;DR
TakaraOS is a microkernel operating system written in Rust. Microkernel architecture is a design that separates the kernel into small, modular components, each of which has a specific set of responsibilities. TakaraOS is designed to be **small**, **secure**, and **efficient**, making it an ideal choice for embedded systems, IoT devices, and other applications that require a small operating system footprint.

One of the unique features of TakaraOS is that it runs [WebAssembly](https://webassembly.org/) (Wasm) code at `ring 0`. ring 0 is the lowest privilege level in a microkernel architecture, which means that Wasm code can run directly on the microkernel, without needing to go through the traditional system call interface. This allows TakaraOS to execute code **faster** and with less overhead than other operating systems.

TakaraOS is written in Rust, a programming language known for its memory safety and low-level control. Rust's strong type system and ownership model make it an excellent choice for an operating system, as it allows developers to write efficient, secure, and reliable code. Additionally, Rust's cargo package manager makes it easy to manage dependencies and build packages, simplifying the process of developing and maintaining TakaraOS.

As a microkernel, TakaraOS is designed to be **highly modular**, with each component responsible for a specific function. The microkernel itself is responsible for basic tasks such as inter-process communication, memory management, and device drivers. Other components, such as the file system, network stack, and user interface, run as user-level processes, communicating with the microkernel via a message-passing interface.

TakaraOS has been designed with **security** in mind, with features such as memory protection, process isolation, and fine-grained access control. The microkernel's small size and modular design also make it easier to audit and verify, reducing the risk of security vulnerabilities.

In summary, TakaraOS is a microkernel operating system written in Rust, designed to be small, secure, and efficient. Its unique feature of running Wasm code at ring 0 makes it an excellent choice for applications that require high performance and low overhead. TakaraOS's modular design, coupled with Rust's memory safety and ownership model, make it a reliable and secure operating system for embedded systems, IoT devices, and other low-level applications.

## Deeper look at wasm in level
[WebAssembly](https://webassembly.org/) (Wasm) is a binary instruction format for a stack-based virtual machine that is designed to run on a wide range of platforms. One of the key advantages of Wasm is that it can be used with a variety of programming languages, making it a versatile technology for building applications.

With TakaraOS, Wasm can be run at ring 0, which means that it can be used to build low-level system components such as device drivers, memory management, and inter-process communication. This is possible because **Wasm code can be compiled to a format that is directly executable on the microkernel**, without needing to go through the traditional system call interface.

The ability to run Wasm at ring 0 has a number of benefits.
1. First, it **allows developers to write system components in a wide range of programming languages**, including C++, Rust, and even JavaScript. This means that developers can use the language that is best suited to the task at hand, without being restricted to a specific language.
2. In addition, running Wasm at ring 0 means that **system components can be written as self-contained modules that can be loaded and unloaded at runtime**. This makes it easier to update and maintain the operating system, as modules can be updated without needing to restart the entire system. It also allows developers to experiment with new system components, without needing to modify the core operating system.

Overall, the ability to run Wasm at ring 0 makes TakaraOS a highly versatile and flexible operating system, capable of running a wide range of programming languages and self-contained system components. This, combined with the microkernel architecture and Rust programming language, makes TakaraOS a highly secure, efficient, and reliable operating system for low-level applications.
