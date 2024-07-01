# 16-Bit-Cirsim-Computer
![16-Bit-Computer](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/d76dfa85-a093-4c33-b695-6e8722d19df8)
 This is a 16 Bit Computer, build withing the Framework of the Cirsim Circuitry software. Given Machine code for Compiled ARM64 code. This computer-circuit will execute those commands. Below I will explain what each image, and circuitry component is responsible for.

 # Register

 <img width="132" alt="Register" src="https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/634dd0be-724d-4005-8d9a-3fc5358469cb">

This is the Register Component of the Circuit. It is responsible for storing data/values that we provide it. At a basic level, this component is made up of Finite State Machines (FSM) which can be used to store bits in a circuit.

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

# ALU1

This is found on the Right side of the Full 16-Bit-Computer image. This unit is reponsible for any opperation that is needed to be performed. The Instruction-Decoder will feed it a 4-Bit C value, this value could perform anything from simple addition to logical shifts to branching calculations. 

# Program Counter

This is found on the middle-left of the main 16-Bit-Computer image. This is a list of instructions that the program needs to execute in order.

# Timing - Circuit

![Timing](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/1d223f7e-e4d0-422c-8997-315e5afc0479)

This whole computer functions on a manual clock, depending on when the clock tick is High or Low, the circuit needs to know when to fetch commands, and execute them. That is what this Circuit Component is repsonsible for.

# Fields

![Fields](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/b4ab31cb-73e6-40ac-85b5-2a20be71a441)

This component is featured in both the "Decoder" and "Read/Write(rw)" components. 

This circuitry compenent receives 16-bits of binary code as Input. This code represents a specific instruction that the computer wants to perform. This component's main fuction, is to split this instruction code into spefic "Fields" (Hence the name). For Example: The top 3-bits (13,14,15) are directed into the output F. This tells our circuit what Type of instruction it is, which later on tells our circuit to select specific outputs from this. If these bits are 000, this is a Format 2 opperation, and will result in an Add/Subtract result. So only the required fields for those opperations will be used, others will be ignored.

# Read/Write(rw)

![Read:Write](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/cc2120d8-0ba9-446d-959a-9c6d63e79a80)

This is a Simple component used within the "Decoder" component, its purpose is to tell our Register-Circuit when it should Write to a register, and when it should read from one.

# Cond

![Cond ](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/5b61e408-2210-4363-a08f-77ed23cb0ea1)

This Component Checks the Given input Condition, and feeds back into the Program Counter. This can be used in branching instructions

# Decoder

![Decoder](https://github.com/TheReedMiller/16-Bit-Cirsim-Computer/assets/174283892/eeb04ddd-0636-4382-9007-74312cfecc24)

This component is shown in the Top-Left of the "16-Bit-Computer" image, and this is the detailed circuitry behind it.

This component takes a binary instruction from the M1 Memory. And depending on what the instruction is, decodes it, and passes the data to the respective places. For example: If this program was to add register 1 to register 2 and store the result in register 0. The A and B inputs to the ALU would be set to the values in registers 1 and 2 respectively. Then the ALU input of the Register-Component would be set to register 0, and the input W would be true, resulting in the value being added, and stored in r0.

# What I learned

While this was very difficult to execute. It taught me a lot about how the basis of computing. While coding in any other language like Python or C++, it helps me understand what is going on inside of a computer and within its memory. Such as variable addition or even when using pointers/arrays.
