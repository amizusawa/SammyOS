include ../Makefile.vars

BUILD_DIR = ../build/drivers
C_SRCS = $(wildcard *.c)
HEADERS = $(wildcard *.h)
C_OBJS = $(C_SRCS:.c=.o)
BUILD_C_OBJS = $(foreach file, $(C_OBJS), $(BUILD_DIR)/$(file))

all: $(BUILD_C_OBJS)

$(BUILD_DIR)/%.o: %.c $(HEADERS)
	@ mkdir -p $(BUILD_DIR) 
	i386-elf-gcc $(CFLAGS) -ffreestanding -c $< -o $@
