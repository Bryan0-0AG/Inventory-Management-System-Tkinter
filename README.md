# 📦 Inventory Management System with Tkinter

> Python desktop application to manage product inventories with a graphical interface, Excel persistence, and real-time data visualization.

---

## 📋 Description

This project is an **inventory management system** developed in Python, combining a graphical interface built with **Tkinter** and data storage in **Excel** files via **pandas**. It allows adding, removing, updating, and subtracting products from an inventory, reflecting changes immediately in a secondary visualization window.

The project is oriented toward practical learning of object-oriented programming, file handling with pandas, and UI development with Tkinter.

---

## 🗂️ Project structure

Inventory-Management-System-Tkinter/
│
├── Main.py                  # Inventory logic (classes and CRUD operations)
├── Interfaz.py              # Main graphical interface with Tkinter
├── Visualización_deDatos.py # Secondary real-time data visualization window
├── .gitignore               # Files ignored by Git
└── LICENSE                  # MIT License

> Inventories are automatically saved in an `Inventarios/` folder created in the project directory.

---

## ⚙️ Features

- **Add product** — Registers a new product with name, price, and quantity. If it already exists, adds the specified quantity.
- **Subtract product** — Reduces the quantity of an existing product. If the amount exceeds current stock, asks for confirmation before proceeding.
- **Delete product** — Completely removes a product from the inventory.
- **Update quantity** — Directly modifies the quantity of an existing product.
- **Update price** — Modifies a product's price without altering its stock.
- **Real-time visualization** — A secondary window displays the inventory table (name, price, quantity) and updates automatically after each operation.
- **Excel persistence** — All data is saved to an `.xlsx` file inside the `Inventarios/` folder, preserving state between sessions.

---

## 🖥️ Graphical interface

The application opens **two simultaneous windows**:

| Window | Description |
|---|---|
| **Main window** (`Interfaz.py`) | Form with name, price, and quantity fields, plus buttons for each operation. |
| **Data window** (`Visualización_deDatos.py`) | Real-time table showing all products in the active inventory. |

---

## 🚀 Installation and usage

### Requirements

- Python 3.8+
- The following libraries:

pip install pandas openpyxl

> `tkinter` is included by default in the standard Python installation.

### Run the application

python Interfaz.py

This will automatically open both the main management window and the data visualization window.

---

## 🧱 Code architecture

The project follows an object-oriented approach, separating responsibilities into three modules:

**`Main.py`** defines two main classes:
- `nuevo_producto` — Represents a product with a name and price.
- `nuevo_inventario` — Manages the Excel file and exposes the inventory's CRUD methods.

**`Interfaz.py`** builds the GUI with Tkinter, instantiates the inventory, and connects each button to its corresponding action, also triggering the visual update after each operation.

**`Visualización_deDatos.py`** maintains a second Tkinter window that reads the Excel file and rebuilds the product table every time `actualizar_visualizacion_datos()` is called.

---

## 🛠️ Technologies used

- **Python** — Main language
- **Tkinter** — Desktop graphical interface
- **pandas** — Reading and writing data in Excel
- **openpyxl** — Engine for `.xlsx` file support

---

## 📄 License

This project is under the **MIT** license. See the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Bryan0-0AG**  
Personal project to learn Python, OOP, and desktop graphical interfaces.