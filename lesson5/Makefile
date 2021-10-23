# version 5
# 多级目录makefile
.PHONY: clean

CC=gcc
CFLAGS=-Wall -g
BIN=main


SUBDIR = $(shell ls -d */)
ROOTSRC = $(wildcard *.c)
ROOTOBJ = $(ROOTSRC:%.c=%.o)
SUBSRC = $(shell find $(SUBDIR) -name '*.c')
SUBOBJ = $(SUBSRC:%.c=%.o)
	
$(BIN): $(ROOTOBJ) $(SUBOBJ)
	$(CC) $(CFLAGS) -o $(BIN) $(ROOTOBJ) $(SUBOBJ)

#%.o:%.c
.c.o:
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(BIN) $(ROOTOBJ) $(SUBOBJ)
