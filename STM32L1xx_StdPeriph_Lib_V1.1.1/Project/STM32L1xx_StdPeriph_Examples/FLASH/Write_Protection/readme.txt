/**
  @page FLASH_Write_Protection FLASH Write Protection example
  
  @verbatim
  ******************** (C) COPYRIGHT 2012 STMicroelectronics *******************
  * @file    FLASH/Write_Protection/readme.txt 
  * @author  MCD Application Team
  * @version V1.1.1
  * @date    13-April-2012
  * @brief   Description of the FLASH Write Protection example.
  ******************************************************************************
  *
  * Licensed under MCD-ST Liberty SW License Agreement V2, (the "License");
  * You may not use this file except in compliance with the License.
  * You may obtain a copy of the License at:
  *
  *        http://www.st.com/software_license_agreement_liberty_v2
  *
  * Unless required by applicable law or agreed to in writing, software 
  * distributed under the License is distributed on an "AS IS" BASIS, 
  * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  * See the License for the specific language governing permissions and
  * limitations under the License.
  *
  ******************************************************************************
   @endverbatim

@par Example Description 

This example provides a description of how to enable and disable the write protection
for the STM32L1xx FLASH memory:

- Enable Write protection: 
   To enable the Write Protection, uncomment the line "#define WRITE_PROTECTION_ENABLE"
   in main.c file.  
   To Enable the write protection of the STM32L1xx Flash, the user has to call 
   FLASH_OB_WRPConfig function.
   The parameter of this function will define the number of pages to be protected 
   and the state of the specified FLASH (ENABLE).
   To load the new option byte values, a system Reset is necessary, for this, the
   function FLASH_OB_Launch() is used.
 
- Disable Write protection:
   To disable the Write Protection, uncomment the line "#define WRITE_PROTECTION_DISABLE"
   in main.c file.
   To Disable the write protection of the STM32L1xx Flash, the user has to call 
   FLASH_OB_WRPConfig function.
   The parameter of this function will define the number of pages to be unprotected 
   and the state of the specified FLASH (DISABLE).
   To load the new option byte values, a system Reset is necessary, for this, the
   function FLASH_OB_Launch() is used.
   
- Program the selected pages:
  To program the desired pages (if the flash is not write protected) uncomment 
  the line  "#define FLASH_PAGE_PROGRAM" in main.c file. 

If the desired pages are not write protected, an erase and a write operation are
performed.
  
@par Directory contents 

  - FLASH/Write_Protection/stm32l1xx_conf.h    Library Configuration file
  - FLASH/Write_Protection/stm32l1xx_it.c      Interrupt handlers
  - FLASH/Write_Protection/stm32l1xx_it.h      Interrupt handlers header file
  - FLASH/Write_Protection/main.c              Main program
  - FLASH/Write_Protection/system_stm32l1xx.c  STM32L1xx system source file
  
@note The "system_stm32l1xx.c" is generated by an automatic clock configuration 
      system and can be easily customized to your own configuration. 
      To select different clock setup, use the "STM32L1xx_Clock_Configuration_V1.1.0.xls" 
      provided with the AN3309 package available on <a href="http://www.st.com/internet/mcu/family/141.jsp">  ST Microcontrollers </a>
         
@par Hardware and Software environment

  - This example runs on STM32L1xx Ultra Low Power High-, Medium-Density and Medium-Density Plus Devices.
  
  - This example has been tested with STMicroelectronics STM32L152D-EVAL (STM32L1xx 
    Ultra Low Power High-Density) and STM32L152-EVAL (STM32L1xx Ultra Low 
    Power Medium-Density) evaluation board and can be easily tailored to any 
    other supported device and development board.
      
@par How to use it ? 

In order to make the program work, you must do the following :
 - Copy all source files from this example folder to the template folder under
   Project\STM32L1xx_StdPeriph_Templates
 - Open your preferred toolchain 
 - Rebuild all files and load your image into target memory
 - Run the example

@note
- Ultra Low Power Medium-density devices are STM32L151xx and STM32L152xx 
  microcontrollers where the Flash memory density ranges between 64 and 128 Kbytes.
- Ultra Low Power Medium-density Plus devices are STM32L151xx, STM32L152xx and 
  STM32L162xx microcontrollers where the Flash memory density is 256 Kbytes.
- Ultra Low Power High-density devices are STM32L151xx, STM32L152xx and STM32L162xx 
  microcontrollers where the Flash memory density is 384 Kbytes.
    
 * <h3><center>&copy; COPYRIGHT STMicroelectronics</center></h3>
 */


