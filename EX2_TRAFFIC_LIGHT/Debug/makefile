################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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


BUILD_ARTIFACT_NAME := EX2_TRAFFIC_LIGHT
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
EX2_TRAFFIC_LIGHT.elf \

MAP_FILES += \
EX2_TRAFFIC_LIGHT.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
EX2_TRAFFIC_LIGHT.list \

OBJCOPY_HEX += \
EX2_TRAFFIC_LIGHT.hex \


# All Target
all: main-build

# Main-build Target
main-build: EX2_TRAFFIC_LIGHT.elf secondary-outputs

# Tool invocations
EX2_TRAFFIC_LIGHT.elf EX2_TRAFFIC_LIGHT.map: $(OBJS) $(USER_OBJS) C:\Users\minhl\OneDrive\Documents\STUDY\HK221\Vi\ xu\ li\SMT32\LAB1\EX2_TRAFFIC_LIGHT\STM32F103C6UX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "EX2_TRAFFIC_LIGHT.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\minhl\OneDrive\Documents\STUDY\HK221\Vi xu li\SMT32\LAB1\EX2_TRAFFIC_LIGHT\STM32F103C6UX_FLASH.ld" --specs=nosys.specs -Wl,-Map="EX2_TRAFFIC_LIGHT.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

EX2_TRAFFIC_LIGHT.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "EX2_TRAFFIC_LIGHT.list"
	@echo 'Finished building: $@'
	@echo ' '

EX2_TRAFFIC_LIGHT.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "EX2_TRAFFIC_LIGHT.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) EX2_TRAFFIC_LIGHT.elf EX2_TRAFFIC_LIGHT.hex EX2_TRAFFIC_LIGHT.list EX2_TRAFFIC_LIGHT.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
