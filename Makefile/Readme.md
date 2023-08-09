# Uma introdução a Makefiles

## Uma visão geral do utilitário `make`

O utilitário `make` determina automaticamente quais partes de um programa grande precisam ser recompiladas e emite comandos para recompilá-las. Este tutorial descreve o GNU make, que foi implementado por Richard Stallman e Roland McGrath. O desenvolvimento desde a versão 3.76 tem sido feita por Paul D. Smith.

Os exemplos que mostro aqui estão implementados em C++, mas você pode usar `make` com qualquer linguagem de programação cujo compilador possa ser executado com um comando shell. De fato, `make` não se limita a programas. Você pode usá-lo para descrever qualquer tarefa em que alguns arquivos devem ser atualizados automaticamente de outros sempre que os outros forem alterados.

## Uma introdução a Makefiles

Você precisa de um arquivo chamado *makefile* ou *Makefile* para dizer ao `make` o que fazer. Na maioria das vezes, o makefile informa ao `make` como compilar e vincular um programa.

Quando o make recompila o editor, cada arquivo fonte C++ alterado deve ser recompilado. Se um arquivo de cabeçalho foi alterado, cada arquivo fonte C++ que inclui o arquivo de cabeçalho deve ser recompilado. Cada compilação produz um arquivo objeto correspondente ao arquivo fonte. Finalmente, se algum arquivo fonte foi recompilado, todos os arquivos de objeto, criados recentemente ou salvos de compilações anteriores, devem ser vinculados para produzir o novo código executável.

Este tutorial mostra apenas uma pequena parte do que é possível fazer com o `make`. Ele pretende ser um guia inicial para que você possa criar de forma rápida e fácil seus próprios makefiles para projetos de pequeno a médio porte.

