TARGET := test2
SRC := $(TARGET).c
OBJ := $(TARGET).o
SOBJ := libdlink.so

CFLAGS := -g -Wall
LFLAGS := -lm -pthread
CC := gcc $(CFLAGS) $(LFLAGS)


all : $(SRC) $(OBJ) $(SOBJ)

.c.o:
	$(CC) -c $^
$(SOBJ):
	gcc -shared display.c -fPIC -o $(SOBJ)
	export LD_LIBRARY_PATH="/home/cpi2301/ensyu2"
	gcc -o $(TARGET)  $(SRC) -L. -ldlink

clean:
	rm -f $(TARGET) $(OBJ) $(SOBJ)

