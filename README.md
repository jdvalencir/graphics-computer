# graphics-computer

Course exercises for a computer graphics class, written in plain Java (Swing/AWT, no external dependencies). The repository collects small programs that draw lines with Bresenham's algorithm, render 2D objects loaded from text files, apply 2D transformations interactively, and a small linear algebra library for points, vectors and matrices.

## Features

- **bresenham**: Bresenham line drawing on a Swing panel, including a "wheel" made of lines drawn every 10 degrees around the origin.
- **object2d**: reads a 2D object from a text file (vertex count, vertex coordinates, edge count, edge index pairs) and draws it. Sample files: `home.txt`, `gancho.txt`.
- **transformations2d**: translation, scaling and rotation of a 2D object using 3x3 matrices (homogeneous coordinates), controlled from the keyboard:
  - `W` / `A` / `S` / `D`: move up / left / down / right
  - `Q` / `E`: scale up (1.2) / down (0.8)
  - `R` / `T`: rotate clockwise / counter-clockwise
- **mathGc**: `Point3`, `Point4`, `Vector3`, `Matrix3x3`, `Matrix4x4`. Includes matrix-matrix and matrix-point multiplication, and vector cross product, dot product, magnitude and normalization. `Main` prints a demo of each. `EcParSegRec` is an empty placeholder class.
- **drawitems**: `DrawItems` helper for drawing items.

## Tech stack

- Java (Swing / AWT)
- No build tool; no `package.json`, Makefile or Dockerfile in the repo

## Project structure

```
bresenham/          Bresenham line algorithm and wheel demo
object2d/           Draw an object from a text file
transformations2d/  Keyboard-driven 2D transformations
mathGc/             Points, vectors, 3x3 and 4x4 matrices
drawitems/          Drawing helper
```

## Getting started

Requires a JDK. Each folder is a Java package with its own `Main` class. From the repository root:

```sh
javac bresenham/*.java
java bresenham.Main

javac object2d/*.java
java object2d.Main

javac transformations2d/*.java
java transformations2d.Main

javac mathGc/*.java
java mathGc.Main
```

Compiled `.class` files are ignored by git.

## Context

Coursework for a computer graphics course ("graphics computer"), by the repository owner.

## License

MIT, see [LICENSE](LICENSE).
