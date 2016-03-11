# rebobinar

## What's it about?

`rebobinar` is a virtual machine that works on an persistent RAM. Instead of
changing the RAM on each operation, instead a new copy of the RAM is created.
This sounds wasteful, but through the power of tries, the amount of extra space
and time that is needed on each operation is proportional to the size of a
pointer rather than the size of the RAM.

The benefit of this approach is that as many past states as needed can be saved.
Hence, "snapshots" of state can be taken. This makes time random-access! That
is, programs running on the `rebobinar` virtual machine can be "run backwards"
in some sense, and any arbitrary state in the past revisited.

## Why the name?

`rebobinar` is Spanish for "rewind".

## What's the architecture?

While it would be nice for `rebobinar` to implement an established VM, like the
LLVM bytecode, the current architecture implemented is a simple machine language
in Julia macro-like syntax.

### Architecture Details

Currently supported operations are: none yet
