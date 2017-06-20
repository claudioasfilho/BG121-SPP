################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include kit_flashpwr/BRD4302A/subdir.mk
-include emlib/subdir.mk
-include device/EFR32_B_1_1_B/gcc/subdir.mk
-include bgapi/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: BG121-SPP.axf

# Tool invocations
BG121-SPP.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM C Linker'
	arm-none-eabi-gcc -g -gdwarf-2 -mcpu=cortex-m4 -mthumb -T "/Users/clfilho/SimplicityStudio/v4_workspace/BG121-SPP/linker/GCC/efr32bg1b232f256gm56.ld" -Xlinker -no-enum-size-warning -Xlinker -no-wchar-size-warning -Xlinker --gc-sections -Xlinker -Map="BG121-SPP.map" -mfpu=fpv4-sp-d16 -mfloat-abi=softfp -o BG121-SPP.axf "./application_properties.o" "./ble-callback-stubs.o" "./ble-callbacks.o" "./gatt_db.o" "./main.o" "./retargetio.o" "./retargetserial.o" "./spp_client_main.o" "./spp_server_main.o" "./bgapi/dmadrv.o" "./bgapi/em_adc.o" "./bgapi/em_ldma.o" "./bgapi/em_leuart.o" "./device/EFR32_B_1_1_B/gcc/startup_efr32bg1b.o" "./emlib/em_cmu.o" "./emlib/em_cryotimer.o" "./emlib/em_gpio.o" "./emlib/em_i2c.o" "./emlib/em_msc.o" "./emlib/em_rtcc.o" "./emlib/em_system.o" "./emlib/em_usart.o" "./kit_flashpwr/BRD4302A/mx25flash_spi.o" "./src/InitDevice.o" "/Applications/Simplicity Studio.app/Contents/Eclipse/developer/sdks/gecko_sdk_suite/v1.0//protocol/bluetooth_2.3/lib/EFR32BG1B/EABI/stack.a" "/Applications/Simplicity Studio.app/Contents/Eclipse/developer/sdks/gecko_sdk_suite/v1.0//protocol/bluetooth_2.3/lib/EFR32BG1B/EABI/binstack.o" "/Applications/Simplicity Studio.app/Contents/Eclipse/developer/sdks/gecko_sdk_suite/v1.0//protocol/bluetooth_2.3/lib/EFR32BG1B/GCC/bgapi.a" "/Applications/Simplicity Studio.app/Contents/Eclipse/developer/sdks/gecko_sdk_suite/v1.0//protocol/bluetooth_2.3/lib/EFR32BG1B/EABI/binbootloader.o" -lm -Wl,--start-group -lgcc -lc -lnosys -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

	@echo 'Building hex file: BG121-SPP.hex'
	arm-none-eabi-objcopy -O ihex "BG121-SPP.axf" "BG121-SPP.hex"
	@echo ' '

	@echo 'Building bin file: BG121-SPP.bin'
	arm-none-eabi-objcopy -O binary "BG121-SPP.axf" "BG121-SPP.bin"
	@echo ' '

	@echo 'Building s37 file: BG121-SPP.s37'
	arm-none-eabi-objcopy -O srec "BG121-SPP.axf" "BG121-SPP.s37"
	@echo ' '

	@echo 'Running size tool'
	arm-none-eabi-size "BG121-SPP.axf"
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) BG121-SPP.axf
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
