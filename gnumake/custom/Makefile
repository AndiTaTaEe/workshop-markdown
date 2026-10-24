
CC = gcc
CFLAGS = -Wall -Wextra -O2
parts_variable = part1.c part2.c

# declare phony targets
.PHONY: all clean parts

# all rule
all: greeting parts
	./greeting
	./parts

# clean rule
clean:
	rm -f greeting parts

# rule for compiling greeting.c
greeting: greeting.c
# compile with different flags based on the compiler
ifeq ($(CC), gcc)
	$(CC) $(CFLAGS) -o $@ $^
else
	$(CC) -o $@ $^
endif

# rule for compiling part1.c and part2.c into an executable called parts
parts: $(parts_variable) header.h
	$(CC) $(CFLAGS) -o $@ $^

# function to print the files of the custom directory
pwd_files := $(shell ls)
print_files:
	@echo "Files in the custom/ directory:"
	@echo "$(pwd_files)"


