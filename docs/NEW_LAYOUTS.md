# New Track Layouts

This document describes the three new example track layouts that have been added to demonstrate various crossing configurations.

## 1. Double Vertical Loop (double_vertical_loop.txt)

**Purpose**: Demonstrates a big loop with two central vertical sections and multiple crossings

**Specifications**:
- Grid Size: 28x16
- Total Crossings: 4
- Pattern: Large rectangular outer loop with two parallel vertical tracks through the center

**Layout Description**:
```
┌────────────────────────────┐
│     │           │          │
│     X           X          │
│     │           │          │
│     │           │          │
│     │           │          │
│     │           │          │
│     │           │          │
│     │           │          │
│     │           │          │
│     X           X          │
│     │           │          │
└────────────────────────────┘
```

**Crossing Locations**:
- Top left: (10,3)
- Top right: (17,3)
- Bottom left: (10,12)
- Bottom right: (17,12)

**Use Cases**:
- Testing multiple crossings in a single layout
- Demonstrating parallel track sections
- Complex route planning with multiple intersection points

## 2. Cross Junction (cross_junction.txt)

**Purpose**: Demonstrates a central crossing with horizontal and vertical tracks forming a plus/cross pattern

**Specifications**:
- Grid Size: 22x14
- Total Crossings: 5
- Pattern: Rectangular outer loop with horizontal and vertical tracks through the middle

**Layout Description**:
```
┌──────X──────────────┐
│      │              │
│      │              │
X──────X──────────────X
│      │              │
│      │              │
│      X              │
└─────────────────────┘
```

**Crossing Locations**:
- Central: (10,6)
- Top edge: (10,3)
- Bottom edge: (10,10)
- Left edge: (4,6)
- Right edge: (17,6)

**Use Cases**:
- Testing central intersection points
- Demonstrating cross-pattern routing
- Edge crossing behavior

## 3. Grid Network (grid_network.txt)

**Purpose**: Demonstrates an internal grid pattern with multiple crossings

**Specifications**:
- Grid Size: 24x16
- Total Crossings: 12 (4 interior + 8 edge)
- Pattern: Rectangular outer loop with 2x2 internal grid

**Layout Description**:
```
┌─────X──────X──────┐
│     │      │      │
X─────X──────X──────X
│     │      │      │
│     │      │      │
X─────X──────X──────X
│     │      │      │
│     X      X      │
└────────────────────┘
```

**Crossing Locations**:
Interior Grid:
- (9,6), (14,6)
- (9,9), (14,9)

Edge Crossings:
- Top: (9,3), (14,3)
- Bottom: (9,12), (14,12)
- Left: (3,6), (3,9)
- Right: (20,6), (20,9)

**Use Cases**:
- Testing complex grid patterns
- Multiple simultaneous crossings
- Network-style track layouts
- Advanced routing scenarios

## How to Use These Layouts

### Loading in Code

```java
// Load any of the new layouts
GameWorld.RailwayWorldData data = GameWorld.loadDefaultLayout("layouts/double_vertical_loop.txt");
// or
GameWorld.RailwayWorldData data = GameWorld.loadDefaultLayout("layouts/cross_junction.txt");
// or
GameWorld.RailwayWorldData data = GameWorld.loadDefaultLayout("layouts/grid_network.txt");
```

### Testing Different Layouts

You can modify which layout is loaded by editing the filename in `GameWorld.loadDefaultLayout()` calls or by specifying the layout file path directly.

## Design Considerations

All layouts follow these principles:
1. **Complete Tracks**: All track sections connect properly (no dead ends)
2. **Proper Crossings**: All intersection points are explicitly marked with CROSSING commands
3. **Edge Connections**: Inner tracks properly connect to outer loop via crossings
4. **Balanced Layout**: Symmetrical or well-balanced track arrangements
5. **Clear Paths**: The main PATH forms a complete loop that trains can follow

## Layout Format Reference

For creating your own custom layouts, see:
- [LAYOUT_FORMAT.md](LAYOUT_FORMAT.md) - Complete format specification
- [USING_LAYOUTS.md](USING_LAYOUTS.md) - Guide to creating and using layouts

## Comparison with Existing Layouts

| Layout | Size | Crossings | Complexity | Pattern Type |
|--------|------|-----------|------------|--------------|
| figure8.txt | 21x15 | 2 | Medium | Figure-8 |
| simple_oval.txt | 15x10 | 0 | Simple | Oval loop |
| large_loop.txt | 25x18 | 0 | Simple | Large rectangle |
| **double_vertical_loop.txt** | 28x16 | 4 | High | Double vertical |
| **cross_junction.txt** | 22x14 | 5 | Medium | Cross pattern |
| **grid_network.txt** | 24x16 | 12 | Very High | Grid pattern |

The new layouts significantly expand the variety and complexity of available track configurations.
