# **Secure Access System with STM32**

This project implements a password-based secure access system designed with an **STM32F401RE** microcontroller. The system manages access using a matrix keypad and provides visual feedback through an LCD display and LEDs. A motor (simulating an electronic lock) is activated when the correct password is entered.

## **Key Features**
- **Secure Password Entry**: A 4x4 matrix keypad allows users to enter a password.
- **Password Verification**: The microcontroller compares the user input with a predefined password.
- **Visual Feedback**:  
  - An LCD screen displays instructions and status messages (e.g., "Enter Password," "Access Granted").
  - A green LED lights up when the correct password is entered.
- **Motor Activation**: A DC motor is triggered via an L293D driver, simulating a door lock mechanism.
- **Extensibility**: The system can be expanded with additional technologies like RFID or Bluetooth communication.

## **Technologies Used**
- **STM32CubeMX**: Used to configure the STM32F401RE pins and generate initialization code.
- **Proteus 8 Professional**: Circuit simulation, including the keypad, LCD, LED, and motor.
- **STM32F401RE Microcontroller**: The system's core, responsible for input processing and peripheral management.

## **Diagrams and Screenshots**
### **Proteus Circuit Diagram**
![Proteus Diagram](5.PNG)

### **Pin Configuration in STM32CubeMX**
![Pin Configuration](configurationpins.PNG)

### **Clock Configuration in STM32CubeMX**
![Pin Configuration](clock.PNG)

## **How to Use This Project**
1. **Simulation in Proteus**:
   - Open the simulation file in Proteus.
   - Run the simulation to test functionality.
2. **Deployment on STM32**:
   - Import the CubeMX configuration into STM32CubeIDE.
   - Compile and upload the code to an STM32F401RE board.
3. **Interacting with the System**:
   - Enter the password using the matrix keypad.
   - Observe visual feedback (LEDs, LCD screen).
   - If the password is correct, the motor will activate.

## **Project Structure**
- **/Proteus**: Contains Proteus simulation files.
- **/CubeMX**: CubeMX configuration files.
- **/Code**: Generated and modified source code for STM32.

## **Possible Improvements**
- Adding a buzzer to signal errors or success.
- Implementing dual authentication with RFID or biometrics.
- Adding Bluetooth/Wi-Fi connectivity for remote control and monitoring.
- Introducing a temporary lockout after multiple failed attempts.
