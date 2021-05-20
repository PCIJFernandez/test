pruebaArchivos: pruebaArchivos.c
	gcc pruebaArchivos.c -o pruebaArchivos

delivery_semaforo: MonitoresBuffer.c delivery_semaforo.c conio.c
	gcc -c -Wall -pedantic MonitoresBuffer.c -o MonitoresBuffer.o
	gcc -c -Wall -pedantic conio.c -o conio.o
	gcc -Wall -pedantic delivery_semaforo.c MonitoresBuffer.o conio.o -lrt -pthread -o delivery_semaforo

borrarMemoriaSemaforos: borrarMemoriaSemaforos.c
	gcc -Wall -pedantic borrarMemoriaSemaforos.c -lrt -pthread -o borrarMemoriaSemaforos

all: borrarMemoriaSemaforos delivery_semaforo pruebaArchivos

clean:
	rm -fr *.o pruebaArchivos delivery_semaforo borrarMemoriaSemaforos puntuacion.txt
