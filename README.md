# Jewellery Manufacturing Automation

This project automates key processes in a jewellery manufacturing business, focusing on inventory management and order processing to increase efficiency.

## Features

- **Inventory Management:** Automates tracking of gold inventory, updates inventory with received gold, and alerts when inventory is low.
  
- **Order Processing:** Automates billing for jewellery orders, including costs for Rhodium polish, stones, hallmarking, labor, and GST.

## Quick Start

1. **Inventory Management:**
   - Initialize the inventory with gold in stock.
   - Update inventory with gold received or used in production.

   ```python
   inventory = Inventory(gold_store=1000.0)
   inventory.update_gold_store(100.0, "add")
   inventory.update_gold_store(50.0, "subtract")
