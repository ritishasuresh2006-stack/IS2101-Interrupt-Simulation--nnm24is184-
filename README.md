# IS2101-Interrupt-Simulation--nnm24is184-

# Description
This project simulates the working of an Interrupt Controller that manages interrupt requests (IRQs) from multiple I/O devices based on priority and masking.
It demonstrates how interrupt priorities and masking affect device handling in a computer system.

# Features
Three simulated devices:
Keyboard — high priority
Mouse — medium priority
Printer — low priority
Interrupt requests are generated (randomly over time).
The interrupt controller always serves the highest‐priority pending interrupt that is unmasked.
Supports masking/unmasking of any device at runtime (so that its interrupts are ignored while masked).
Logs each ISR execution timestamp and maintains an execution history.
Clear console outputs showing when interrupts are triggered, queued, handled, or ignored.

# File / Code Structure
interrupt-controller-simulation
├── Main.java                
├── InterruptController.java 
├── Device.java              
├── README.md                
└── report.pdf              

# Usage / Running the Program
Requirements
Java JDK (version 8 or above)
Command-line or IDE of your choice

Compile
```bash
javac Main.java InterruptController.java Device.java
java Main
```

# Sample Output
KEYBOARD → ISR Completed at 14:23:11  
MOUSE Ignored (Masked)  
PRINTER → ISR Completed at 14:23:13  
...
--- ISR Log ---  
14:23:11 - KEYBOARD executed  
14:23:13 - PRINTER executed  
...

# Output
<img width="524" height="592" alt="Screenshot (146)" src="https://github.com/user-attachments/assets/e6213faf-6321-48b6-813e-ed6a9122a2d7" />

# Conclusion
This simulation shows how an interrupt controller can manage multiple I/O devices using priority and masking. It highlights how higher-priority, unmasked interrupts are served first, and how devices can be ignored if masked. Through multithreading and logging, it offers a simple yet effective model of interrupt handling in a system.
