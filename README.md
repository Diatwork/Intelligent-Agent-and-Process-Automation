# Jewellery Manufacturing Business Process Automation

This project automates key processes within a gold jewellery manufacturing business, including inventory management and order processing. The automation streamlines manual tasks such as billing, invoice generation, and inventory management, leading to reduced costs, error rates, and increased productivity.

## Features

- **Inventory Management:** Automated tracking of gold inventory, including adding and subtracting gold based on orders and supplier deliveries. Alerts when inventory falls below a specified threshold, with options to place orders with suppliers.
  
- **Order Processing:** Facilitates the creation of orders for different types of jewellery items (Rings, Bangles, Bracelets). Automatically calculates the final billing amount, including costs for Rhodium polish, stones, hallmarking, labor, and GST.

- **Billing and Invoice Generation:** Automates the calculation of order amounts based on the current gold rate, applied services, and additional charges. Generates a final invoice and writes order details to a CSV file for record-keeping.

## Classes and Methods

### 1. `Inventory`
Manages the gold inventory for the jewellery manufacturing process.

- **`__init__(self, gold_store: float)`**: Initializes the inventory with a specified amount of gold.
- **`update_gold_store(self, gold_sent: float, operation: str)`**: Updates the inventory based on the gold sent or received. Operations include 'subtract' and 'add'.
- **`print_gold_store(self)`**: Prints the current amount of gold in the inventory.

### 2. `Order`
Handles the creation and processing of jewellery orders.

- **`__init__(self, item_type: str, pieces: int, gold_sent: float, order_req: float)`**: Initializes an order with details such as item type, number of pieces, and gold requirements.
- **`calculate_amount(self, gold_rate: float)`**: Calculates the final amount based on the gold rate, additional services like Rhodium polish, stones, hallmarking, and labor charges.

### 3. `Instock`
Advanced inventory management with supplier interaction for replenishing gold stock.

- **`__init__(self, gold_store: float, threshold: float = 50.0)`**: Initializes inventory management with a starting amount of gold and a threshold below which a replenishment order is suggested.
- **`display_inventory(self)`**: Displays the current gold inventory.
- **`update_inventory(self, gold_amount: float)`**: Adds new gold to the inventory and logs the update.
- **`log_inventory_change(self, action: str, gold_amount: float)`**: Logs inventory changes to a CSV file, tracking actions like receiving gold or placing orders.
- **`check_inventory(self)`**: Checks if inventory falls below the threshold and suggests placing an order.
- **`place_order(self)`**: Handles placing orders with suppliers when inventory is low.
- **`manage_inventory(self)`**: Manages inventory by handling incoming gold and checking if a replenishment is needed.

## Usage

### 1. **Initialize Inventory**

```python
inventory = Inventory(gold_store=1000.0)  # Starting with 1000 grams of gold
