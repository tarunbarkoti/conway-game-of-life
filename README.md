# Conway's Game of Life Interactive Visualizer  
**Second Trimester Final Project**  
*CCE - IIT Mandi (Minor in Computer Science & Engineering)*  

## Project Overview
This Python implementation simulates Conway's Game of Life, a zero-player game that models cellular evolution through simple rules. The visualizer provides an interactive interface to observe pattern evolution with save/load functionality.

## Implementation Details

### Core Components
- **Model**: Uses a 2D array (`width × height`) or set of coordinates to track live cells
- **Rules Engine**: Applies Conway's classic rules with immutable updates (generates new board each step)
- **Visualization**: Choose between Pygame (for performance) or Tkinter (for simplicity)

### Key Features
1. **Interactive Controls**:
   - Play/Pause simulation (Spacebar)
   - Single-step through generations (N key)
   - Clear grid (C) or randomize (R)
   - Save/Load patterns (S/L keys)

2. **Pattern Persistence**:
   - Save/Load patterns as coordinate lists in `patterns.txt`
   - Supports comments (lines starting with #)

3. **Runtime Statistics**:
   - Current generation count
   - Live cell counter
   - Adjustable simulation speed

## Simulation Rules
Each cell's fate is determined by its 8 neighboring cells:

| Neighbor Count | Current State | Next State |
|----------------|---------------|------------|
| < 2           | Alive         | Dies       |
| 2-3           | Alive         | Survives   |
| > 3           | Alive         | Dies       |
| Exactly 3     | Dead          | Born       |

## Usage

```bash
python life.py [--width W] [--height H] [--fps F]
```

## Command Line Options
1. **--width**: Grid width (default: 60)
2. **--height**: Grid height (default: 30)
3. **--fps**: Frames per second (default: 10)

## Example
```bash
python life.py --width 40 --height 20 --fps 6
```

## Testing

Pre-verified with standard patterns:

• **Blinker**: Oscillator pattern (period 2)\
• **Glider**: Spaceship pattern (moves diagonally)

## Expected Output

```plaintext
┌ Game of Life ──────────────────────────────┐
│ Controls: Space=Play/Pause  N=Step  C=Clear │
│ Generation: 42       Live Cells: 117        │
└─────────────────────────────────────────────┘
```

## Development Requirements

Python 3.x
Pygame (recommended) or Tkinter
argparse module (built-in)\




**(Author: Tarun Barkoti)**
