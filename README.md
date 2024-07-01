# 16-Bit-Cirsim-Computer
![16-Bit-Computer](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/d76dfa85-a093-4c33-b695-6e8722d19df8)
 This is a 16 Bit Computer, build withing the Framework of the Cirsim Circuitry software. Given Machine code for Compiled ARM64 code. This computer-circuit will execute those commands. Below I will explain what each image, and circuitry component is responsible for.

 # M1 - Memory Bank
 ![M1-MemoryBank](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/52ce8ca0-9474-4dc6-80a9-d30c7d72fd2e)
 This image shows the input to the M1 component of the Circuit. By accessing this you are able to upload Machine Code (Hex), that instructs the computer to execute dasks just as a ARM64 compiler would.

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


# Fields
This component is featured in both the "Decoder" and "Read/Write" images/components. 

This circuitry compenent receives 16-bits of binary code. This code represents a specific instruction that the computer wants to perform. This component

# Decoder

This component is shown in the Top-Left of the "16-Bit-Computer" image, and the detailed circuitry behind it is shown in the "Decoder" image.

This component takes a binary instruction from the
    
