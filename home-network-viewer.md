---
layout: default
title: Home Network Diagram (Interactive Viewer)
---

[← Back to Home Network & Home Lab](./home-network.md)

# Home Network & Lab Architecture Diagram (Interactive Viewer)

Use the controls below to zoom and pan around the diagram.  
Scroll the mouse wheel over the diagram to zoom, and drag to pan.

<div class="diagram-viewer">
  <div class="diagram-controls">
    <button type="button" id="diag-zoom-in">Zoom In</button>
    <button type="button" id="diag-zoom-out">Zoom Out</button>
    <button type="button" id="diag-reset">Reset</button>
  </div>

  <div id="diagram-container">
    <img
      id="diagram-image"
      class="diagram-viewer-img"
      src="./images/network/home-network-lab-overview.png"
      alt="Home Network & Lab Architecture Diagram"
    />
  </div>
</div>

<!-- Panzoom library -->
<script src="https://cdn.jsdelivr.net/npm/@panzoom/panzoom@4.6.1/dist/panzoom.min.js"></script>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    const container = document.getElementById('diagram-container');
    const image     = document.getElementById('diagram-image');

    const zoomInBtn  = document.getElementById('diag-zoom-in');
    const zoomOutBtn = document.getElementById('diag-zoom-out');
    const resetBtn   = document.getElementById('diag-reset');

    const panzoom = Panzoom(image, {
      maxScale: 10,
      minScale: 1,
      contain: 'outside'
    });

    container.addEventListener('wheel', function (event) {
      event.preventDefault();
      panzoom.zoomWithWheel(event);
    }, { passive: false });

    zoomInBtn.addEventListener('click', () => panzoom.zoomIn());
    zoomOutBtn.addEventListener('click', () => panzoom.zoomOut());
    resetBtn.addEventListener('click', () => panzoom.reset());
  });
</script>

---

[← Back to Home Network & Home Lab](./home-network.md)