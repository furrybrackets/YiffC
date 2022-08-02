# YiffC
A high-level IR language designed to be a frontend for [LibFirm](https://github.com/libfirm/libfirm), since LLVM is shitty.


## Running YiffC from the command-line

First, build Yiff with the `cli` option. Then, run:

```
yiff $(file)
```

## Textual Example

YiffC compiles to ultra-minimal bytecode, but it has a textual format. This format is designed to be easily generated, parsed, and readable.

```
# -03
i32 func(i32 @x, i32 @y) {
    i32 @1 = @x + @y;
    
    return @1; // supports utf-8 variable names.
};

i32 v.name = 10; // yes, really.

struct StructName { // only thing not supported in names are { or } or " " (space)
   float θ;
   float μ;
};
```

# Acknowledgements

This project uses LibFirm, which is LGPL licensed. Here is a link to the source code (note: it's really cool *yip*, check it out!):

[Source Code](https://github.com/libfirm/libfirm).

**This project is not endorsed or directly affiliated with the licensees or maintainers of "LIBFIRM".**
