# Kernel Tutorial

I really enjoy learning about and understanding lower-level computer systems. While [OSDEV wiki](http://wiki.osdev.org/Main_Page) is a fantastic resource, I've really struggled with many of their tutorials. So, I thought it would be nice to take things that I've gotten working at put them into a git-based tutorial.

This series isn't even close to as thorough as what you'll find over at OSDev. But, it's all geared towards getting something working, with OS X as your development environment. If you're a linux user, I think you'll be able to adapt most of these instructions to your system fairly easily.

# Tooling

While each tutorial part will include installation steps, here's a list of everything needed for all steps in one place. First and foremost, install Xcode to get it's suite of command line tools.

    brew install qemu
    brew install xorriso
    brew install nasm

We're going to be building an ELF executable, but OS X uses Mach-O. Clang is a really great cross-compiler, but we also need a cross-linker, which OS X does not include by default. At one point, I was able to install the gcc ELF bintuils directly from homebrew, but lately I've been unable to find a default that works. I'd love some pointers here. I used this:

    brew install https://raw.githubusercontent.com/Gallopsled/pwntools-binutils/master/osx/binutils-i386.rb

# Tutorial Parts

Everything is broken up into a series of steps, which you can find under [tutorial-parts](tutorial-parts).

1. [Basic Bootloader](tutorial-parts/1-grub.md)
2. [Basic 32-bit Kernel](tutorial-parts/2-basic-kernel.md)

# Contributing

It would be wonderful to see issues/PRs opened for problems you experience with this tutorial. I'd be excited even to just hear you tried it out.