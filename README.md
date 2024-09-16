# Embedded_Systems
#Project Setup Procedure:

Step 1 : I have downloaded STM32cudeIDE from the following link 
https://www.st.com/en/development-tools/stm32cubeide.html#get-software.

Step 2 : Upon installation, I began by creating a new file    File -> New -> STM32 Project -> press 'Enter'.

 
 
Step 3: After that, I chose the board ‘Nucleo-F411RE’.





Step 4: Then I have given ‘LAB1_KEERTHI’ as project name.


 
Key Steps:
Step 5: I configured PA5 as ‘GPIO_Output’ and named it ‘LED’ for the pin.




Step 6: I have actually set the ‘GPIO output level High’ in system core under PA5 and saved the file.

 
Compilation and Execution:
	After step-6, for the experimental setup, I connected the microcontroller board to the laptop via USB cable.
	After the experimental setup , I went to src -> main.c and then I wrote the code in the line 99 -104 with a delay of 500 inside while loop as shown in the below figure.



	Then , I build the main.c by clicking the icon as highlighted in below figure.

 
	The console window shows the compilation result. Upon successful compilation , the led starts blinking with 500ms delay.



	Below is a video demonstration of LED Blinking with 500ms (milli-seconds) delay.
https://drive.google.com/file/d/1jpBnuUX46IO7lstNoPhQz_rwcGl6pRpI/view?usp=driv e_link
 
Challenges Encountered and Their Resolutions:
Problem-1:
	This is the first challenge that I faced while configuring the LED Pin. Even after configuring the LED Pin, it’s not been reflected in the main.c code.

Problem-2:
	This is the second challenge that I faced, while building the code.

Resolution:
	I did not save after configuration due to which this problem arose. To solve this issue, I went back to the pin configuration and here I reconfigured the pin PA5(LED) mode to GPIO OUTPUT, set output level High and Saved it. Then configured pin got reflected in the main.c code.
	The problem-2 error is because it has LED_pin mentioned in the code. As, LED_pin is not configured before, it showed an error. Once after configuring and saving the pin configuration. The error got resolved.
 
Configuring the Pin to Illuminate the LED:

1.	Pin Selection: I have selected the pin PA5.



2.	Pin Configuration: I configured the pin as GPIO Output pin and named it as LED. In the system Core on GPIO I have defined that this GPIO level should be High. The Configured pin is reflected in the main.c as shown below.

 
3.	Connection: Once after configuring, I have connected the board with laptop and then in main.c, I wrote the code inside while loop to blink an Led with 500ms delay and follow up the same by successfully running this code.so finally, the green color led started blinking with a delay of 500ms.
{
HAL_GPIO_WritePin(LED_GPIO_Port,LED_Pin,0); // 0 indicates LED off HAL_Delay(500); // DELAY HAL_GPIO_WritePin(LED_GPIO_Port,LED_Pin,1); // 1 indicates LED on HAL_Delay(500); // DELAY

}

So, basically the LED glows for 500ms (as given in the delay) and gets off for 500ms (as given in the delay) continuously until the board is connected to the laptop.




LED BLINKING WITH 1500ms DELAY:
	I have followed the above steps and set the delay to 1500ms.




	Below is a video demonstration of LED Blinking with 1500ms (milli-seconds) delay.
https://drive.google.com/file/d/1h8AFKSwJLotGY59VNJYy269LRqn7H4 Mj/view?usp=drive_link
