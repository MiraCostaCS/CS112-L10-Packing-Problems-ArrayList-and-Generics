## 📋 Project Assessment: Lab #10 - ArrayList + Generics (Packing Problems)

### 1. Development & Workflow
- [ ] **Targeted Modifications:** All work confined to `Transfer.java` and `Inventory.java` without modifying `Main` or `Setup`.
- [ ] **Commit Messages:** Descriptive and incremental commits tracking data migration, generic setup, search, and editing functionality.

### 2. Functional Requirements

#### Step 1: ArrayList Migration & Setup (`Transfer.java`)
- [ ] **List Declarations:** Created parameterized `ArrayList` fields: `List<Food> foodList`, `List<Parts> partsList`, and `List<Supplies> suppliesList`.
- [ ] **Constructor Conversion:** Updated `Transfer` default constructor to populate the lists from the provided base arrays.
- [ ] **Display Verification:** Uncommented `printLists()` multi-line comment block and verified output via **View Lists**.

#### Step 2: Item Addition & Special Research (`Transfer.java`)
- [ ] **`addItems()` Implementation:** Added `List.add()` logic to append user-input objects to the corresponding lists.
- [ ] **STS-96 Mission Data Added:**
    - [ ] **Food:** Pears (Perishable: True, Qty: 20), Hot Sauce (Perishable: False, Qty: 5), Chocolate (Perishable: False, Qty: 30).
    - [ ] **Parts:** Copper Tube (Qty: 50, ID: 10053), Kevlar Strap (Qty: 30, ID: 10040), Titanium Bolts (Qty: 45, ID: 10032).
    - [ ] **Supplies:** Sleep Mask (Qty: 10), Book (Qty: 5), Ellen Ochoa's Flute (Qty: 1).

#### Steps 3 & 4: Generic Inventory Setup (`Inventory.java` & `Transfer.java`)
- [ ] **Bounded Type Parameter:** Defined `Inventory<T extends Supplies>` class header to enforce type bounds and grant access to `Supplies` getters.
- [ ] **Class Members:** Implemented instance variables, constructors, getters, and setters within `Inventory`.
- [ ] **Object Instantiation:** Instantiated parameterized `Inventory` objects in `Transfer` (`Inventory<Food>`, `Inventory<Parts>`, `Inventory<Supplies>`).

#### Steps 5 & 6: Generic Search & Item Removal
- [ ] **`searchByName()` Implementation (`Inventory.java`):**
    - [ ] Method signature: accepts `List<T> items` and `String name`.
    - [ ] Searches list using `getName()` and returns matching index (or `-1` if not found).
- [ ] **`removeItems()` Integration (`Transfer.java`):** Uses `searchByName()` to retrieve target indices and calls `List.remove()` to drop items.

#### Steps 7 & 8: Generic Quantity Management
- [ ] **`checkQty()` Implementation (`Inventory.java`):**
    - [ ] Method signature: accepts `List<T> items`, `int desiredQuantity`, and `String name`.
    - [ ] Reuses `searchByName()` to find index and updates target item quantity.
- [ ] **`editQuantity()` Integration (`Transfer.java`):** Implemented `checkQty()` inside `editQuantity()` and verified adjustments:
    - [ ] **Food Updates:** Bread (Qty: 20), Orange (Qty: 30), Protein Bar (Qty: 30).
    - [ ] **Parts Updates:** Steel Truss (Qty: 4), Solar Panel (Qty: 25), Steel Panel (Qty: 4).
    - [ ] **Supplies Updates:** Laptop (Qty: 9), Sleep Restraint (Qty: 5), First Aid Kit (Qty: 5).

### 3. Code Quality & Standards
- [ ] **Generics Best Practices:** Explicit use of bounded type parameters (`<T extends Supplies>`) and correct diamond operator syntax.
- [ ] **Encapsulation:** Private fields maintained across generic classes with public accessor/mutator methods.
- [ ] **Naming & Conventions:** Consistent `camelCase` naming for methods/variables and standard Java formatting.
