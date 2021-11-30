################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
matrix-keypad-3.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
matrix-keypad-3.list \

OBJCOPY_HEX += \
matrix-keypad-3.hex \

OBJCOPY_BIN += \
matrix-keypad-3.bin \


# All Target
all: matrix-keypad-3.elf secondary-outputs

# Tool invocations
matrix-keypad-3.elf: $(OBJS) $(USER_OBJS) C:\Users\lukav\STM32CubeIDE\workspace_1.3.0\matrix-keypad-3\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "matrix-keypad-3.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\lukav\STM32CubeIDE\workspace_1.3.0\matrix-keypad-3\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="matrix-keypad-3.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

matrix-keypad-3.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "matrix-keypad-3.list"
	@echo 'Finished building: $@'
	@echo ' '

matrix-keypad-3.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "matrix-keypad-3.hex"
	@echo 'Finished building: $@'
	@echo ' '

matrix-keypad-3.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "matrix-keypad-3.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
