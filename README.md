# Enso Advent of Code 2025

[![CI](https://github.com/JaroslavTulach/AOC-2025-Enso/actions/workflows/enso.yml/badge.svg)](https://github.com/JaroslavTulach/AOC-2025-Enso/actions/workflows/enso.yml)

Get ready for [Advent of Code 2025](https://adventofcode.com/2025) by
solving its tasks for  in [Enso](http://enso.org) low/no code environment.

<img width="711" height="662" alt="project template" src="https://github.com/user-attachments/assets/826d298a-3048-4d49-b2c8-fd7304373916" />

## Fork Your Own Copy

First of all fork [this repository](https://github.com/JaroslavTulach/AOC-2025-Enso.git)
to your own github account.

<img width="1215" height="317" alt="fork" src="https://github.com/user-attachments/assets/d600ec36-89d5-4f6f-b262-8c015f243be1" />

Then you'll get your own repository URL:

<img width="920" height="583" alt="url" src="https://github.com/user-attachments/assets/7f0985cc-daa1-4e9e-8869-fa375e5a3d2e" />

## Setup & Execution

Get this repository to your local computer. Use `git` to clone it using
the URL obtained in previous step. I can clone mine with:
```bash
$ git checkout https://github.com/JaroslavTulach/AOC-2025-Enso.git
$ cd AOC-2025-Enso
$ ls -1
Dec00
README.md
```
Let's download [Enso](http://enso.org) now. Enso can run on Linux, Windows, MacOSX.
The following is tested on [2025.2.4](https://github.com/enso-org/enso/releases/tag/2025.2.4) version.

<img width="826" height="320" alt="Add Folder" src="https://github.com/user-attachments/assets/75952184-9f9f-42a3-8b69-7f628a9e316f" />

Add the `AOC-2025-Enso` folder into your IDE. Then you'll see the skeletal
`Dec00` project. You can open the project and play with it, but
before you start solving real [AoC 2025](https://adventofcode.com/2025) tasks,
it is **suggested to duplicate** the project...

<img width="918" height="639" alt="Duplicate & Rename" src="https://github.com/user-attachments/assets/7aa72b7b-52e2-4f96-a6bf-a852d5719062" />

and **rename it** for example to `Dec01` for the first task of the [AoC 2025](https://adventofcode.com/2025).

## The Structure of the Project

A typical [Advent of Code](https://adventofcode.com/) quiz starts with a specified
input. The `Dec00` project provides support for that by reading the input from
`data/input.txt` file:
```
$ find Dec00/*
Dec00/data
Dec00/data/input.txt
Dec00/package.yaml
Dec00/src
Dec00/src/Main.enso
```
When you duplicate the project, just locate `Dec37/data/input.txt` and put the
quiz input into that file.

The main program code is then in `Dec00/src/Main.enso`. It reads the `input.txt`
and then processes it somehow:
```ruby
main =
    file1 = Enso_Project.enso_project.data/"input.txt"
    data = Data.read file1 ..Delimited
    any1 = data.parse ['Column 1'] type=..Integer
    result1 = any1.compute ..Sum
    Runtime.assert (result1 == 13) "Expecting this result"
```
this logic needs to be adjusted according to the actual
[Advent of Code](https://adventofcode.com/) quiz. But using `Data.read` is
almost always a good start. Keep that and remove the subsequent lines.

Good luck solving [Advent of Code 2025](https://adventofcode.com/2025) with [Enso](http://enso.org)!

## Continuous Integration Check

The github repository contains [automatic CI check](./.github/workflows/enso.yml)
to verify your changes to the repository are correct. There is **Actions** tab
in the repository:

<img width="723" height="376" alt="GitHub Actions" src="https://github.com/user-attachments/assets/61f2b177-2491-4717-811f-8290a9693283" />

it contains list of all _workflow runs_. As soon as a change is integrated (via `git push`)
to your GitHub repository a check for all projects prefixed `Dec` in the repository
is triggered to **verify correctness of your code**.

<img width="1241" height="437" alt="CI Runs" src="https://github.com/user-attachments/assets/a4be8c3d-ffca-4d6d-8476-6f6bb7e396f3" />

If a _workflow run_ is **green** then your code changes are sane. Use this
_continuous integration_ check to never break code that you have written in the
past!
