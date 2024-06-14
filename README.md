# Verification_AMBA-APB
## Design and Functional Verification of AMBA-APB protocol.
### Mritunjoy Kar Pial

 Dept. of Electrical and Electronic Engineering  
   Chittagong University of Engineering and Technology, Bangladesh

# Table of Contents 
- [Introduction of AMBA](#Introduction-of-AMBA)  
- [APB Specification](#APB-Specification)
  * [APB Interface Diagram](#APB-Interface-Diagram)
  * [APB Signal Description](#APB-Signal-Description)
  * [APB State Diagram](#APB_State_Diagram)
  * [APB Operating States](#APB_Operating_States)
    * [Write transfer](#Write_transfer)
    * [Read transfer](#Read_transfer)
-  [Testplan](#Testplan)
-  [Simulation results of APB design](#Simulation-results-of-APB-design)
-  [Conclusion](#Conclusion)
- [Acknowledgement](#Acknowledgement)
- [References](#References)

# Introduction of AMBA
- An AMBA-based microcontroller consists of high-performance system backbone bus, which is able to sustain the external memory bandwidth, on which the High-performance ARM processor and DMA devices reside, along with a bridge to narrower APB bus. The APB protocol is designed to connect low-bandwidth peripherals to the main system bus.


    ![Alt](Images/image1.png)

# APB Specification
- A low-cost interface, optimized for minimal power consumption and reduced interface complexity.
- The APB interface is not pipelined and is a simple, synchronous protocol. Every transfer takes at least two cycles to complete.
- APB peripherals are typically connected to the main memory system using an APB bridge.
## APB Interface Diagram
- Simple Interface diagram of APB Slave

  ![Alt](Images/image2.png)

## APB Signal Description

 **PCLK:** The rising edge of PCLK times all transfers on the APB.   
 **PRESETn:** Connected directly to System bus. The APB reset signal is active LOW.  
 **PADDR:** 32 bit address bus and is driven by thr peripheral bus bridge unit.  
 **PSEL:** Select, the APB bridge unit generates this signal to each peripheral bus slave. It indicates that, slave device is selected and transfer is required. There is a PSEL for each slave.
 **PENABLE:** This signal indicates the second and subsequent cycles of an APB transfer.   
 **PWRITE:**  APB write enables when [HIGH](#HIGH) and APB read enables when [LOW](#LOW).    
 **PWDATA:**  32 bits Write data PWRITE is HIGH.     
 **PREADY:**  Ready To extend an APB transfer.    
 **PRDATA:**  32 bits Read data and PWRITE is LOW.   
 **PSLAVERR Slave error:** This signal indicates a transfer failure. 
