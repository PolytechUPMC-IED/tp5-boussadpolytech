CC=gcc
CFLAGS= -O3 -Wall -funroll-loops
LDLIBS= -lpng
SRC =  printer.c pbm2eps9.c
OBJ =$(SRC:.c=.o)

all:pbm2png pbm2eps9

pbm2png: pbm2png.c
		$(CC) $(CFLAGS) -s -o  $@ $< $(LDLIBS)


pbm2eps9: $(OBJ)
	$(CC) -s -o $@ $(OBJ)


%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $<	


clean:
	rm -f $(OBJ) pbm2png pbm2eps9
