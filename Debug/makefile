################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
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
all: Mi_primer_proyecto.axf

# Tool invocations
Mi_primer_proyecto.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\matia\Documents\MCUXpressoIDE_11.4.0_6237\workspace\lpc_board_nxp_lpcxpresso_1769\Debug" -L"C:\Users\matia\Documents\MCUXpressoIDE_11.4.0_6237\workspace\lpc_chip_175x_6x\Debug" -Xlinker -Map="Mi_primer_proyecto.map" -Xlinker --cref -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "Mi_primer_proyecto_Debug.ld" -o "Mi_primer_proyecto.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) Mi_primer_proyecto.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "Mi_primer_proyecto.axf"; # arm-none-eabi-objcopy -v -O binary "Mi_primer_proyecto.axf" "Mi_primer_proyecto.bin" ; # checksum -p LPC1769 -d "Mi_primer_proyecto.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
