CC = gcc
CFLAGS = -Wall -Wpedantic -Wextra -ggdb -std=c99 -I..

run: main
	valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./main

main: main.c far_away_malloc.c
	$(CC) $(CFLAGS) far_away_malloc.c main.c -o main

clean:
	rm -rf main
