# makefile for building the emulator

# General definitions

CC := gcc
AR := ar
RM := rm -f

CFLAGS := -Wall -Wextra -ansi -pedantic -std=c99 \
          $(shell sdl2-config --cflags) $(EXTRA_CFLAGS)
LDFLAGS := $(shell sdl2-config --libs)

INCLUDES :=
LIBS := -lm -lSDL2

OBJS :=

TARGET := gtemu libgtemu.a

all: $(TARGET)

include module.mk

# Pattern rules

gtemu: $(OBJS) main.o
	$(CC) $(LDFLAGS) -o $@ $^ $(LIBS)

libgtemu.a: $(OBJS)
	$(AR) rcs $@ $^

%.o: %.c
	$(CC) $(CFLAGS) $(INCLUDES) -c $< -o $@

clean:
	$(RM) $(TARGET) $(OBJS) main.o

.PHONY: all clean
