.RECIPEPREFIX = >
CC = g++
CFLAGS = -O3 -fopenmp
O = OBJ/
HEADERS = macros.h cvector.h cmatrix.h

default: sgfdm2d
all: sgfdm2d fdm1d

sgfdm2d: $(O)main.o $(O)sgfdm2d.o
> $(CC) -o $@ $^ $(CFLAGS)

fdm1d: $(O)fdm1d.o
> $(CC) -o $@ $^ $(CFLAGS)

$(O)%.o: %.cpp Makefile $(HEADERS)
> @mkdir -p $(O)
> $(CC) -o $@ -c $< $(CFLAGS)

clean:
> rm -f sgfdm2d fdm1d $(O)*
