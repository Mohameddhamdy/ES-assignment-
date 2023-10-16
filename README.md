# ES-assignment-
c
#include <stdint.h>
#include "stm32f4xx.h" // Include the appropriate CMSIS header for your microcontroller

// Function to enable interrupts globally
void enable_interrupts(void) {
    __enable_irq();
}

// Function to initialize the NVIC
void NVIC_Init(void) {
    // Set interrupt priority levels if necessary
    // NVIC_SetPriority(IRQn_Type IRQn, uint32_t priority);

    // Enable desired interrupts
    // NVIC_EnableIRQ(IRQn_Type IRQn);
}

// Interrupt handler for a specific interrupt
void EXTI0_IRQHandler(void) {
    // Handle the interrupt
    // ...
    // Clear the interrupt flag if necessary
    // EXTI_ClearITPendingBit(EXTI_Line0);
}

// Configure the interrupt vector table
void NVIC_Configuration(void) {
    // Set the interrupt vector table base address
    SCB->VTOR = NVIC_VectTab_FLASH;

    // Set the interrupt vector table offset if necessary
    // SCB->VTOR |= 0x20000;
}

int main(void) {
    // Initialize the NVIC
    NVIC_Configuration();
    NVIC_Init();

    // Enable interrupts
    enable_interrupts();

    while (1) {
        // Main program loop
    }
}
