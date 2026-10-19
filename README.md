# Motor de Cenas 3D em OpenGL

Projeto da unidade curricular de **Computação Gráfica**. Inclui um gerador de
primitivas geométricas e um motor OpenGL que renderiza cenas descritas em XML,
com transformações, câmaras, iluminação e texturas.

## Componentes

- `generator/` — gera modelos `.3d` (plano, caixa, esfera, cone e Bézier).
- `engine/` — motor de renderização OpenGL/GLUT.
- `test files/` — cenas, texturas e resultados das quatro fases.
- `utils/` — estruturas geométricas e escrita de ficheiros de modelo.

## Dependências

Em Ubuntu/Debian:

```bash
sudo apt update
sudo apt install cmake g++ freeglut3-dev libdevil-dev libtinyxml2-dev
```

## Compilar e executar

```bash
cmake -S . -B build
cmake --build build
./build/generator sphere 1 10 10 esfera.3d
./build/engine "test files/test_files_phase_4/solar_system.xml"
```

No motor, `1`, `2` e `3` alternam entre os modos sólido, wireframe e pontos.
`O` ativa a câmara orbital, `F` regressa à câmara fixa e `ESC` encerra a
aplicação.

## Documentação

- [`MANUAL.txt`](MANUAL.txt) contém os comandos e controlos completos.
- [`relatorioFase4.pdf`](relatorioFase4.pdf) contém o relatório final.
