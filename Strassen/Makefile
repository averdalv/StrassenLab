all: run

clean:
	rm -f src/*.class out/Strassen.jar

Strassen.jar: out/parcs.jar src/*.java
	@javac -cp out/parcs.jar src/*.java
	@jar cf out/Strassen.jar -C src .
	@rm -f src/*.class

run: Strassen.jar
	@cd out && java -cp 'parcs.jar:Strassen.jar' Strassen matrix1.txt matrix2.txt