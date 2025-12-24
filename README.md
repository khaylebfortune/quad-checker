# Quad Checker in Go

## Overview
This project implements a **Quad Checker** program written in Go.  
The program reads an ASCII pattern from standard input and determines which of the predefined quad functions (`quadA`, `quadB`, `quadC`, `quadD`, `quadE`) could have generated that pattern, along with its dimensions.

If the input does not correspond to any known quad pattern, the program reports that it is not a valid quad.

This project focuses on **string manipulation**, **pattern recognition**, and **algorithmic reasoning** using only the Go standard library.

---

## Problem Description
A *quad* is a rectangular ASCII pattern generated using specific border characters depending on the quad type.  
Each quad function produces a rectangle of width `x` and height `y`.

The task of the quad checker is to:
1. Read a pattern from standard input.
2. Determine its width and height.
3. Regenerate all possible quad patterns with those dimensions.
4. Compare the generated patterns with the input.
5. Output which quad(s) match the input pattern.

---

## Supported Quad Types
The program checks against the following quad generators:

- **quadA**
- **quadB**
- **quadC**
- **quadD**
- **quadE**

Each quad type uses different characters for corners, borders, and interior spaces.

---

## Algorithm
1. Read the full input pattern from `stdin`.
2. Split the input into lines to determine:
   - Height (`y`) as the number of lines.
   - Width (`x`) as the length of each line.
3. Validate that:
   - All lines have equal length.
   - Dimensions are positive.
4. Generate patterns for each quad function using `(x, y)`.
5. Compare the generated output with the input pattern.
6. Print all matching quad names and dimensions, or an error message if none match.

---

## How to Run

### Build and Run
Clone the repository and run the program using Go:

```bash
go run .
```
### Example Usage

```bash
printf "o--o\n|  |\no--o\n" | go run .
```
Output:
```text
[quadA] [4] [3]
