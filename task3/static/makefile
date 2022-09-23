.phony: clean
exe_static: fact.o fib.o headers.h.gch main.o  	
	@gcc -o progs main.o ./libtask.a
	@echo "Static library has been created ,ready to run"
fact.o:fact.c
	@gcc -c fact.c
fib.o: fib.c
	@gcc -c fib.c
headers.h.gch: headers.h
	@gcc -c headers.h
	@ar rcs libtask.a fact.o fib.o headers.h.gch
main.o:main.c
	@gcc -c main.c	
run: progs
	@./progs	
	
clean:
	@rm -f *.o *.h.gch *.a progs	
