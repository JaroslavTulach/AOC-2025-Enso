# Enso Advent of Code 2025

[![CI](https://github.com/JaroslavTulach/AOC-2025-Enso/actions/workflows/enso.yml/badge.svg)](https://github.com/JaroslavTulach/AOC-2025-Enso/actions/workflows/enso.yml)

Get ready for [Advent of Code 2025](https://adventofcode.com/2025) by
solving its tasks for  in [Enso](http://enso.org) low/no code environment.

## Fork Your Own Copy

First of all fork [this repository](https://github.com/JaroslavTulach/AOC-2025-Enso.git)
to your github account. 

## Setup & Execution

Get this repository to your local computer. Use `git` to clone it:
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
