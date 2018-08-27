OBJS = cube.o rectangle.o circle.o sphere.o
DEPS = connect.h
colour_start= \e[1;33m #For yellow colour
colour_start1= \e[1;35m #For yellow colour
end =\e[0m For white colour

all:shapes

shapes:$(OBJS) main.c
	@/bin/echo -e "$(colour_start)Targets : $@ $(end)"
	gcc -o $@ $^

%.o: %.c $(DEPS)
	@/bin/echo -e "$(colour_start1) $^ $(end)"
	gcc -o $@ -c $<

clean:
	rm *.o shapes