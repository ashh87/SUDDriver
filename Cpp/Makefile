all: seneyec

seneyec: main.o hid.o
	g++ -Wall -O2 main.o hid.o -o seneyec -ludev -lncurses

main.o: main.cpp
	g++ -Wall -O2 -c main.cpp -o main.o

hid.o: linux/hid.c
	gcc -Wall -O2 -c linux/hid.c -o hid.o
clean:
	rm -rf *.o seneyec
