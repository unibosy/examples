TOPDIR=`pwd`
LIBPATH=${TOPDIR}
LDFLAGS=-Wl,-rpath,$(LIBPATH)


TARGET=demo
.PHONY: all clean
all: $(TARGET)

$(TARGET) : test.o
	gcc -o demo test.o -L. -lagorasdk $(LDFLAGS)
test.o : test.c
	gcc -c test.c -I.
clean :
	rm -f demo test.o
