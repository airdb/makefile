# version 6
# 将每个目录下的文件生成一个可执行文件
# 只有此Makefile的话， 并不能成功执行。  
# 此文件功能，只是将命令，传递给相应的Makefile
# 这个功能已经很强大了！！！ 可完成超大型的工程， 
# 如果test1目录下仍有目录，可借鉴lesson5中的Makefile

SUBDIRS = test1 test2
.PHONY:default all clean $(SUBDIRS)

default:all

all clean:
	$(MAKE) $(SUBDIRS) TARGET=$@

$(SUBDIRS):
	$(MAKE) -C $@ $(TARGET)
