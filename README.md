# 16-Bit-Cirsim-Computer
![16-Bit-Computer](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/d76dfa85-a093-4c33-b695-6e8722d19df8)
 This is a 16 Bit Computer, build withing the Framework of the Cirsim Circuitry software. Given Machine code for Compiled ARM64 code. This computer-circuit will execute those commands. Below I will explain what each image, and circuitry component is responsible for.

 # M1 - Memory Bank
 ![M1-MemoryBank](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/52ce8ca0-9474-4dc6-80a9-d30c7d72fd2e)
 
 This image shows the input to the M1 component of the Circuit. By accessing this you are able to upload Machine Code (Hex), that instructs the computer to execute dasks just as a ARM64 compiler would.

 For Example:
 If I was to compile the following ARM64 code
     mov r1, #3
     mov r2, #5
     add r0, r1, r2
     
After uploading the collowing machine code to the M1 memory bank. My ciruit would execute the following 3 actions
1) Store the number 3 into register 1
![R1](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/d36b0a0b-e796-4253-b16b-1c79e74005aa)

2) Store the number 5 into register 2
![R2](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/d025557a-570e-4a62-a9c7-c09c5ce0a9f3)

3) add the values of register 1 and 2, and store the result in register 0
![R0](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/4ceccc2f-de6b-4441-8eb7-a891e3db0019)

The result will be r0:0008 shown within the R component (Register)
![R0](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/a9b18c30-3041-4d8c-b6da-390b7f3ea8c1)

# Fields
This component is featured in both the "Decoder" and "Read/Write" images/components. 

This circuitry compenent receives 16-bits of binary code. This code represents a specific instruction that the computer wants to perform. This component

# Decoder

This component is shown in the Top-Left of the "16-Bit-Computer" image, and the detailed circuitry behind it is shown in the "Decoder" image.

This component takes a binary instruction from the
    
