################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := NUCLEO_GPIO_Toggle_BUZZER
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
NUCLEO_GPIO_Toggle_BUZZER.elf \

MAP_FILES += \
NUCLEO_GPIO_Toggle_BUZZER.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
NUCLEO_GPIO_Toggle_BUZZER.list \


# All Target
all: main-build

# Main-build Target
main-build: NUCLEO_GPIO_Toggle_BUZZER.elf secondary-outputs

# Tool invocations
NUCLEO_GPIO_Toggle_BUZZER.elf NUCLEO_GPIO_Toggle_BUZZER.map: $(OBJS) $(USER_OBJS) D:\Dai_Hoc\Ki_2_Nam_3\THUC_TAP_CO_SO\CubeIDE\workspace\NUCLEO_GPIO_Toggle_BUZZER\STM32F401RETX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "NUCLEO_GPIO_Toggle_BUZZER.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Dai_Hoc\Ki_2_Nam_3\THUC_TAP_CO_SO\CubeIDE\workspace\NUCLEO_GPIO_Toggle_BUZZER\STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="NUCLEO_GPIO_Toggle_BUZZER.map" -Wl,--gc-sections -static -L"D:\Dai_Hoc\Ki_2_Nam_3\THUC_TAP_CO_SO\CubeIDE\SDK_1.0.3_NUCLEO-F401RE\SDK_1.0.3_NUCLEO-F401RE\lib_stm" --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

NUCLEO_GPIO_Toggle_BUZZER.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "NUCLEO_GPIO_Toggle_BUZZER.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) NUCLEO_GPIO_Toggle_BUZZER.elf NUCLEO_GPIO_Toggle_BUZZER.list NUCLEO_GPIO_Toggle_BUZZER.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
