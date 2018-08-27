IDIR = ../include
ODIR = ../obj

CC = gcc
CFLAGS = -I$(IDIR)

_OBJS = hellomake.o hellofunc.o
OBJS = $(patsubst %,$(ODIR)/%, $(_OBJS))

_DEPS = hellomake.h
DEPS = $(pathsubst %,$(IDIR)/%, $(_DEPS) )


hellomake: $(OBJS)
	$(CC) -o $@ $^ $(CFLAGS)

$(ODIR)/%.o: %.c $(DEPS)
	$(CC) -o $@ -c $< $(CFLAGS)

clean:
	rm $(OBJS) hellomake

