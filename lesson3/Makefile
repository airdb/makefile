.PHONY: clean
BIN=01test 02test
all: $(BIN)
# %.o: %.c功能与.c.o功能相同
%.o: %.c
	gcc -Wall -g -c $< -o $@

.c.o:
	gcc -Wall -g -c $< -o $@

01test: 01test.o
	gcc -Wall -g  $^ -o $@
02test: 02test.o
	gcc -Wall -g  $^ -o $@

clean:
	rm -rf $(BIN) *.o
