# COMPILER_23115060
# ⚡ Coulomb's Law Compiler using Flex & Bison

This project is a **Coulomb's Law Compiler** built using **Flex (Lex) and Bison (Yacc)**. It processes user inputs representing Coulomb's Law expressions and generates **Three Address Code (TAC)** and optimized machine-level instructions.

Coulomb's Law defines the electrostatic force between two charges as:

F=ke*(q1*q2)/(r^2)

where:
- **F** = Electrostatic force (Newtons)
- **ke** = Coulomb’s constant (9 × 10⁹ N·m²/C²)
- **q1, q2** = Charge values (Coulombs)
- **r** = Distance between charges (meters)

---

## 🧩 How It Works

The **lexical analyzer (Flex)** scans the input and extracts numerical values and keywords.  
The **syntax analyzer (Bison)** processes the expressions and computes the output.  
Finally, **optimized Three Address Code (TAC) and machine-level instructions** are generated.

### ✅ Recognized Tokens:

- `COULOMB` → Recognizes a Coulomb’s Law expression.
- 
- `F` → Represents force.
- 
- `ke` → Coulomb's constant.
- 
- `q1, q2` → Charge values.
- 
- `r` → Distance between the charges.
- 
- `;` → Statement terminator.

---

## 💡 Example Execution


🧪 Example  
### 📌 Input:

COULOMB F = 9e9, 1.6 , 1.6 , 3000;



### 📌 Output:

Token: COULOMB (Keyword) 

Token: F (Force Variable)

Token: = (Assignment)

Token: 9e9 (Coulomb Constant)

Token: 1.6 (Charge q1) 

Token: 1.6 (Charge q2)

Token: 3000 (Distance)

Token: ; (End Statement)

📌 Computed Electrostatic Force: F = 2.56 N

🔢 Total Tokens: 8

### 📷 OUTPUT PICS 📸

![OUTPUT (WITH TAC)](https://github.com/user-attachments/assets/69e4011f-a0f6-4990-a4ec-774896345d23)

### 🪟 Windows with MSYS2 🪟

💻 Run in MSYS2 terminal:

pacman -Syu

pacman -S mingw-w64-x86_64-gcc 
flex bison make

## 🛠️ Setup & Usage

### 📌 Requirements:

- **Flex** (Fast Lexical Analyzer)
- 
- **Bison** (Yacc-compatible parser generator)
- 
- **GCC** (C compiler)

### ⚙️ Build Steps:

1. Save the **Flex file** as `lexer.l`
2. Save the **Bison file** as `parser.y`
3. Use the `Makefile` to compile:

### 🤝Bash

make
This will:

Generate lex.yy.c (Flex output)

Generate parser.tab.c and parser.tab.h (Bison output)

Compile everything into an executable named coulomb_compiler



### ▶️ Running the Compiler  

Run the program using:  


./coulomb_compiler


Enter an expression in the following format:


COULOMB F = ke, q1, q2, r;


For example:


COULOMB F = 9e9, 2e-9, 3e-6, 0.1;
The compiler will tokenize the input, generate Three Address Code (TAC), optimize it, and compute the electrostatic force (F).




###  📁 Project Structure

coulomb-compiler/

├── lexer.l           # Lexical analyzer (Flex)

├── parser.y          # Syntax analyzer (Bison)

├── Makefile          # Build script

├── main.o            # Object file

├── coulomb_compiler  # Compiled executable

└── README.md         # Project documentation


###  📝 Notes

Input is case-sensitive (use COULOMB, F, ke, etc.).

Supports both scientific notation (e.g., 9e9) and decimal values.

Requires a semicolon ; at the end of every statement.

Can be extended with error handling, expression trees, and additional optimizations.

### 📜 Author

NAKKA RITHWIK

🎓 B.Tech CSE, NIT Raipur
--23115060
