################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
001Helloworld_semihosting.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
001Helloworld_semihosting.list \

OBJCOPY_BIN += \
001Helloworld_semihosting.bin \


# All Target
all: 001Helloworld_semihosting.elf secondary-outputs

# Tool invocations
001Helloworld_semihosting.elf: $(OBJS) $(USER_OBJS) C:\Users\Diaa\Documents\MCU1-Course\MCU1\001Helloworld_semihosting\STM32F030R8TX_FLASH.ld
	arm-none-eabi-gcc -o "001Helloworld_semihosting.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"C:\Users\Diaa\Documents\MCU1-Course\MCU1\001Helloworld_semihosting\STM32F030R8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="001Helloworld_semihosting.map" -Wl,--gc-sections -static -specs=rdimon.specs -lc -lrdimon --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

001Helloworld_semihosting.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "001Helloworld_semihosting.list"
	@echo 'Finished building: $@'
	@echo ' '

001Helloworld_semihosting.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "001Helloworld_semihosting.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
