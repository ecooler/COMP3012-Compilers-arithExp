This directory contains a couple of test files.

test0.mt test1.mt test2.mt test3.mt test4.mt test5.mt

The above are valid test files for your compiler. The compiler should produce the corresponding files that are also in the directory:

test0.tam test1.tam test2.tam test3.tam test4.tam test5.tam

When you execute the TAM programs, the expected results are:

test0.tam > input 12 > output 479001600
test1.tam > output 21
test2.tam > output 55
test3.tam > input 4 > outputs 2 and 1 (for background, read about the Collatz conjecture)
test4.tam > no output 
test5.tam > output 100

error1.mt is not a correct MT program and can't be compiled to TAM code. Your compiler should ideally produce an error message.
error2.mt has a semicolon that shouldn't be there. Apart from that, it is okay with the convention that `var x` means `var x := 0`. Without the semicolon, it would be fine to treat it as a correct program (not an error). The current version should ideally produce a compile error.
error3.mt (previously test_6.mt) can't be compiled to TAM code. Ideally, your compiler should produce an error message.



