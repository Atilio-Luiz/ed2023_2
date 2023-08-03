# Uma introdução a Makefiles

## Uma visão geral do programa `make`

O utilitário `make` determina automaticamente quais partes de um programa grande precisam ser recompiladas e emite comandos para recompilá-las. Este tutorial descreve o GNU make, que foi implementado por Richard Stallman e Roland McGrath. O desenvolvimento desde a versão 3.76 tem sido feita por Paul D. Smith.

Os exemplos que mostro aqui estão implementados em C++, mas você pode usar `make` com qualquer linguagem de programação cujo compilador possa ser executado com um comando shell. De fato, `make` não se limita a programas. Você pode usá-lo para descrever qualquer tarefa em que alguns arquivos devem ser atualizados automaticamente de outros sempre que os outros forem alterados.

## 