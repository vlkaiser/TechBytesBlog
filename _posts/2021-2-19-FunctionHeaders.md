---
layout: post
title: Useful Function Headers
---

A useful function header template for hardware:


~~~
/******************************************************************************
* @fn		    - nameOfFunction  
* @brief	    - Handles the Control user button presses  
* @param[in]	- GPIO_Pin : GPIO Pin number  
* @return	    - void      
*
* @note	        - Identify which button was pressed and Update data packet  
* 		          GPIO pin defines in main.h  
********************************************************************************/
void nameOfFunction (uint16_t GPIO_Pin)
{
    // Function Actions 
}
~~~
