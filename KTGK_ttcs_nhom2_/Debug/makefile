################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (11.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include SDK_1.0.3_NUCLEO-F401RE/shared/Utilities/subdir.mk
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


BUILD_ARTIFACT_NAME := KTGK_ttcs_nhom2_
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
KTGK_ttcs_nhom2_.elf \

MAP_FILES += \
KTGK_ttcs_nhom2_.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
KTGK_ttcs_nhom2_.list \

OBJCOPY_HEX += \
KTGK_ttcs_nhom2_.hex \

OBJCOPY_BIN += \
KTGK_ttcs_nhom2_.bin \


# All Target
all: main-build

# Main-build Target
main-build: KTGK_ttcs_nhom2_.elf secondary-outputs

# Tool invocations
KTGK_ttcs_nhom2_.elf KTGK_ttcs_nhom2_.map: $(OBJS) $(USER_OBJS) D:\New\ folder\KTGK_ttcs_nhom2_\STM32F401RETX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "KTGK_ttcs_nhom2_.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\New folder\KTGK_ttcs_nhom2_\STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="KTGK_ttcs_nhom2_.map" -Wl,--gc-sections -static -L"D:\SDK_1.0.3_NUCLEO-F401RE\lib_stm" --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

KTGK_ttcs_nhom2_.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "KTGK_ttcs_nhom2_.list"
	@echo 'Finished building: $@'
	@echo ' '

KTGK_ttcs_nhom2_.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "KTGK_ttcs_nhom2_.hex"
	@echo 'Finished building: $@'
	@echo ' '

KTGK_ttcs_nhom2_.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "KTGK_ttcs_nhom2_.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) KTGK_ttcs_nhom2_.bin KTGK_ttcs_nhom2_.elf KTGK_ttcs_nhom2_.hex KTGK_ttcs_nhom2_.list KTGK_ttcs_nhom2_.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
