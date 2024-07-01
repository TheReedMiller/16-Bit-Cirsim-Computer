# 16-Bit-Cirsim-Computer
 This is a 16 Bit Computer, build withing the Framework of the Cirsim Circuitry software. By accessing the M1 Memory Bank within this ciruit. I was able to upload Machine Code (Hex), that instructed this computer to execute dasks just as a ARm64 compiler + 16 Bit Computer would.

 For Example:
 If I was to compile the following ARM64 code
     mov x1, #3
     mov x2, #5
     add x0, x1, x2
After uploading the collowing machine code to the M1 memory bank. My ciruit would execute the following 3 actions
1) Store the number 3 into register 1
2) Store the number 5 into register 2
3) add the values of register 1 and 2, and store the result in register 0

The result will be r0:0008 shown within the R component (Register)

#Decoder

    
