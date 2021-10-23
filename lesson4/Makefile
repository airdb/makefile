.PHONY: clean
CC=gcc
CFLAGS=-Wall -g

BIN=01test 02test 03test 04test
all: $(BIN)
# %.o: %.c功能与.c.o功能相同
# 模式规则      后缀规则
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

.c.o:
	$(CC) $(CFLAGS) -c $< -o $@

01test: 01test.o
	$(CC) $(CFLAGS)  $^ -o $@
02test: 02test.o
	$(CC) $(CFLAGS)  $^ -o $@

03test: 02test.o pub.o
	$(CC) $(CFLAGS)  $^ -o $@

clean:
	rm -rf $(BIN) *.o
