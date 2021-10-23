# version 6
# $@ 规则的目标文件名
# # $< 规则的第一个依赖文件名
# # $^ 规则的所有依赖文件列表 
#
CC = gcc
BIN = test1
OBJS = test1.o

.PHONY: all clean print

all:print $(BIN)

print:
	@echo "----- make all in $(PWD) -----"

$(BIN):$(OBJS)
	$(CC) $(OBJS) -o $@

%.o:%.c
	$(CC) -c $<

clean:
	@echo "----- make clean in $(PWD) -----"
	rm -f $(BIN) $(OBJS)
