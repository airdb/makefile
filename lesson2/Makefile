# version 2
# 相比version1而且更加专业，用了一些自动化变量和自己定义的变量
# $@ 规则的目标文件名
# $< 规则的第一个依赖文件名
# $^ 规则的所有依赖文件列表 
# main: main.o add.o sub.o
# $@  main
# $<  main.o
# $^  *.o
#

OBJECTS = main.o add.o sub.o

.PHONY: clean
# 如果touch add.c， 那么会先执行add.c的编译，时间戳
main: $(OBJECTS)
		gcc -Wall -g $^ -o $@

main.o: main.c
	gcc -Wall -g -c $< -o $@

add.o: add.c add.h
	gcc -Wall -g -c $< -o $@

sub.o: sub.c sub.h
	gcc -Wall -g -c $< -o $@


# 伪目标, 如果是伪目标需要  .PHony: clean
# 不然如果当前目录下刚好有伪目标这个文件，那么就不会执行。
# 错误警告为  make: `clean' is up to date.
clean:
	# 加@表示不打印本条语句，但会执行这条语句
	@echo "begin delete"
	rm -rf main $(OBJECTS)
