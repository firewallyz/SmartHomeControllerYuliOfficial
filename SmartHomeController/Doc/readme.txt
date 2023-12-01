/**
  @page doxygen style readme document for Yuli's SmartHomeController
  
  @verbatim
  ******************** (C) COPYRIGHT 2017 STMicroelectronics *******************
  * @file    SmartHomeController/Doc/readme.txt 
  * @author  Yuli Zhou
  * @brief   Description of the SmartHomeController project
  ******************************************************************************
   @endverbatim

@par Description 

This project showcases a smart home control system ran on a STM32F469i_DISCO board. The system demostrates the following 4 embedded system features:
> Hardware interrupt - The hardware "user button" on the STM board is used to switch on & off any selected room light in the smart home. This is done via interruption which alters
settings in the system. The target light is selected from the GUI. The "user button" can then be used to toggle the light regardless of which page the GUI is currently on. 
> Timer - Lights can be configured to automatically turn off after a certain period of time. They can also be set up to flash at regular intervals. The GUI page currently provides
the option to switch on a light for 6 seconds, The page also allows flashing of the lights with 6 seconds intervals.
> GUI - The entire system can be controlled by the user by an easy-to-use, easy-to-understand graphical user interface. 
> Touch input - No external mouse or app is required to use the GUI, the touch control on the board's built in touchscreen is supported. Navigation is done via on-screen buttons.


@note The 4 built in LEDs are used to simulate lights across a smart house.
      
@note The features are currently spread across multiple projects. The button interrupt is in "SmartHomeController". Timer is in "TIM_TimeBase". GUI and touch input are in TouchGFX.

@note The connection of the LCD reset pin to a dedicated GPIO PH7 instead of the STM32F469 NRST pin may cause residual display on LCD with applications/examples that do not require display.
	  The LCD clear can be ensured by hardware through the boards power off/power on or by software calling the BSP_LCD_Reset() function.

@par Keywords

Smart Home, Controller, Control System, Interrupt, Timer, GUI, Touchscreen

@par Key Files 

  - TIM_TimeBase_Yuli/Src/main.c                 Timer program
  - SmartHomeController/Core/Src/main.cpp        Main program & Unit testor
  


@par Hardware and Software environment

  - This project runs on STM32F469xx devices.
  - Simulated GUI runs on PCs running TouchGFX application,


@par How to use it ? 

For button interrupt and Timer
 - Import project "SmartHomeController" and "TIM_TimeBase" in STM32CubeIDE
 - Build project
 - Run project

For GUI and Touch input
 - Import "MyApplication_1" into TouchGFX
 - Open project and select "Run Simulator"
 */
