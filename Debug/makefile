################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
MS5611_NUCLEO_F070RB.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
MS5611_NUCLEO_F070RB.list \

OBJCOPY_BIN += \
MS5611_NUCLEO_F070RB.bin \


# All Target
all: MS5611_NUCLEO_F070RB.elf secondary-outputs

# Tool invocations
MS5611_NUCLEO_F070RB.elf: $(OBJS) $(USER_OBJS) C:\Users\Administrator\Desktop\CubeIde-Workspace\MS5611_NUCLEO_F070RB\STM32F070RBTX_FLASH.ld
	arm-none-eabi-gcc -o "MS5611_NUCLEO_F070RB.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"C:\Users\Administrator\Desktop\CubeIde-Workspace\MS5611_NUCLEO_F070RB\STM32F070RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="MS5611_NUCLEO_F070RB.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

MS5611_NUCLEO_F070RB.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "MS5611_NUCLEO_F070RB.list"
	@echo 'Finished building: $@'
	@echo ' '

MS5611_NUCLEO_F070RB.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "MS5611_NUCLEO_F070RB.bin"
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
