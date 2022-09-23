.phony: clean
exe_dynamic: fact.c fib.c headers.h main.c  	
	@gcc -shared -fpic -o libtask.so fact.c fib.c headers.h
	@gcc -o progd main.c ./libtask.so
	@echo "Dynamic library has been created ,ready to run"	
run: progd
	@./progd	
	
clean:
	@rm -f *.o *.h.gch *.so progd	
