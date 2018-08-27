COMPILE=gcc

# vpath %.c /home/cgupta3131
all: hello.exe

%.exe: %.o
	gcc -o $@ $^

%.o: %.c
	gcc -c $^

clean:
	rm xhello.exe