# NoteGraph

NoteGraph adds a graph button to Simpl page and pane title bars. It opens a temporary graph centered on that page and shows nearby pages that link to it or are linked from it.

## Features

- Starts with direct connections (depth 1); increase the depth up to 3.
- Distinguishes connections by link direction with arrows.
- Drag the background to pan, use the wheel or zoom controls, and use **Fit** to recenter.
- Select a node to open that page in a new Simpl pane. When Simpl is unavailable, it navigates to the page normally.
- Shows a maximum of 60 pages at a time to keep dense graphs responsive.
- Filters out pages the current user cannot read.
- Uses a local SVG renderer with no external JavaScript libraries.

## Installation

Install the `notegraph` directory under `lib/plugins/notegraph` and enable **NoteGraph** in DokuWiki's Extension Manager if it is not enabled automatically. The title bar button is added when Simpl is active; the plugin's graph data endpoint remains independent of the template.

The graph uses DokuWiki's page-link index for incoming connections and the rendered page instructions for outgoing links. Rebuild or refresh the DokuWiki search index if incoming links appear incomplete.
