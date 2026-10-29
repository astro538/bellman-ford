# Bellman–Ford Algorithm Visualizer

A browser-based learning tool that explains the Bellman–Ford shortest-path algorithm using an animated graph and a step-by-step code walkthrough.

## Learning modes

- **Visualization:** watch edge relaxation steps on a generated directed, weighted graph.
- **Code walkthrough:** follow algorithm steps while relevant code lines and distance/predecessor values are highlighted.
- **Source vertex:** choose a starting vertex and observe how distances are initialized and updated.
- **Playback controls:** run or step through the algorithm and reset the view.

## Algorithm overview

Bellman–Ford computes shortest-path distances from a source vertex in a weighted graph. It repeatedly relaxes edges for up to (V - 1) passes, where (V) is the number of vertices. It supports negative edge weights and can detect a reachable negative-weight cycle with an additional pass.

The tool is intended as an educational visualization; review the implementation before relying on it for other graph inputs or applications.

## Run locally

This project uses plain HTML, CSS, JavaScript, and SVG. No package installation or build step is required.

### Option 1: Open the page

Open `index.html` in a modern browser.

### Option 2: Use a local web server

From the repository root:

```bash
python -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

## Repository structure

```text
bellman-ford/
├── index.html       # Page structure and learning-mode UI
├── css/
│   └── main.css     # Layout, visuals, and animation styles
├── js/
│   └── main.js      # Graph generation, algorithm steps, controls, and rendering
└── README.md
```

## Concepts demonstrated

- Initialization of source distance to zero and all other distances to infinity
- Edge relaxation
- Distance and predecessor tracking
- Repeated passes through the edge list
- Step-by-step algorithm visualization and code mapping

## Limitations

- The current app generates a demonstration graph rather than providing a general graph editor or file import.
- The README does not claim a tested negative-cycle example or validated correctness suite.
- The visualization is for learning and should not be treated as a formal verification of the algorithm implementation.

## Future improvements

Add editable graph inputs, example cases with negative edges and negative cycles, automated test cases, and a visible final shortest path reconstruction.

## License

No explicit license file was identified in the repository when this README was prepared.
