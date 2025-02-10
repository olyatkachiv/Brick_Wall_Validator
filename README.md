# 🧱 Wall Construction Validator

## 📌 Task Definition
This program checks whether a **wall of a given configuration** can be **constructed** using a provided set of bricks.

## 🔄 How the Algorithm Works
1. **Input File Format**:
   - Matrix size (**width × height**) and its content:
     - `0` → Empty space
     - `1` → Part of the wall.
   - Number of available **brick types**.
   - A **list of bricks**, formatted as: `(width, height, quantity)`.

2. **Calculations**:
   - Computes the total **required wall area** (sum of all `1`s in the matrix).
   - Computes the **total available brick cells** by multiplying **width × height × quantity** for each brick type.

3. **Comparison & Output**:
   - If **available brick cells ≥ required wall area** → ✅ `"yes"` (the wall **can** be built).
   - Otherwise → ❌ `"no"` (not enough material to construct the wall).

## 📝 Example Execution
### **Input File 1 (`input_1.txt`)** → Expected Output: `"no"`
- Wall requires **16** cells.
- Available bricks:
  - `2×2` (1 piece) → **4** cells
  - `1×3` (1 piece) → **3** cells
  - `1×4` (1 piece) → **4** cells
- **Total available cells**: `4 + 3 + 4 = 11`
- **Result**: `11 < 16` → `"no"`

### **Input File 2 (`input_2.txt`)** → Expected Output: `"yes"`
- Wall requires **16** cells.
- Available bricks:
  - `2×2` (1 piece) → **4** cells
  - `1×3` (1 piece) → **3** cells
  - `1×4` (1 piece) → **4** cells
  - `3×4` (5 pieces) → **60** cells
- **Total available cells**: `4 + 3 + 4 + 60 = 71`
- **Result**: `71 > 16` → `"yes"`

## 🛠️ Implementation
- **Built with**: **HTML + JavaScript**
- **How it works**:
  - **User uploads a file** via `<input type="file">`
  - **JavaScript processes the data** and calculates the result.
  - **Result is displayed** in `<p id="output">`.

📌 **Author**: _Olha Tkachiv_  
