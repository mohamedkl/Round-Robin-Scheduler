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
RoundRobin_task_scheduler.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
RoundRobin_task_scheduler.list \

OBJCOPY_BIN += \
RoundRobin_task_scheduler.bin \


# All Target
all: RoundRobin_task_scheduler.elf secondary-outputs

# Tool invocations
RoundRobin_task_scheduler.elf: $(OBJS) $(USER_OBJS) F:\work\cv\mk\projects\RoundRobin_task_scheduler\STM32F429ZITX_FLASH.ld
	arm-none-eabi-gcc -o "RoundRobin_task_scheduler.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"F:\work\cv\mk\projects\RoundRobin_task_scheduler\STM32F429ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="RoundRobin_task_scheduler.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

RoundRobin_task_scheduler.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "RoundRobin_task_scheduler.list"
	@echo 'Finished building: $@'
	@echo ' '

RoundRobin_task_scheduler.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "RoundRobin_task_scheduler.bin"
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
