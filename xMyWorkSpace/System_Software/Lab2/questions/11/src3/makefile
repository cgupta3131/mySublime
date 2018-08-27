IDIR = ../include
CC = gcc
CFLAGS= -I$(IDIR)
colour_start= \e[1;33m #For yellow colour
end =\e[0m


ODIR = ../obj
LDIR = ../lib

LIBS = -lm

_DEPS = hellomake.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS)) # Pattern Replacement Text

_OBJ = hellomake3.o hellofunc3.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

$(ODIR)/%.o: %.c $(DEPS)
	@/bin/echo -e "$(colour_start)Targets : $@$(end)"
	@echo "Objects: $^"
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: $(OBJ)
	@echo "Targets: $@"
	@echo "Objects: $(OBJ)"
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

clean:
	rm $(OBJ) hellomake