# Dynamic Wumpus Logic Agent

This project is a web-based Wumpus World logic agent. The agent moves inside a grid world where pits and a Wumpus are placed randomly. The agent does not know the hazard locations at the start. It uses percepts like Breeze and Stench to update its knowledge base and decide which nearby cell is safe.

## Features

- Dynamic grid size using rows and columns
- Random placement of pits and Wumpus
- Percept generation for Breeze and Stench
- Propositional Logic based Knowledge Base
- Resolution Refutation for checking safe cells
- Visual grid interface
- Safe, visited, unknown, and hazard cells shown with colors
- Inference step counter
- Simple browser-based implementation

## Technologies Used

- HTML
- CSS
- JavaScript

## How It Works

The agent starts from the first cell of the grid. When it enters a cell, it receives percepts based on nearby hazards.

If there is a pit near the agent, it receives Breeze.  
If the Wumpus is near the agent, it receives Stench.

The agent adds this information into its Knowledge Base. Before moving to a nearby unvisited cell, it checks whether that cell is safe. It uses resolution refutation to prove that the cell does not contain a pit and does not contain the Wumpus.

If the cell is proven safe, the agent moves there. Otherwise, it avoids that cell.

## Logic Used

The project uses propositional symbols like:

```text
P_r_c = Pit exists at row r and column c
W_r_c = Wumpus exists at row r and column c
