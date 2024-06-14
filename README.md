# Verification_AMBA-APB
## Design and Functional Verification of AMBA-APB protocol.
### Mritunjoy Kar Pial

 Dept. of Electrical and Electronic Engineering  
   Chittagong University of Engineering and Technology, Bangladesh

# Table of Contents 
- [Introduction of AMBA](#Introduction-of-AMBA)  
- [APB Specification](#APB_Specification)
  * [APB Interface Diagram](#APB_Interface_Diagram)
  * [APB Signal Description](#APB_Signal_Description)
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

