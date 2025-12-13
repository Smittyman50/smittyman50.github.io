---
layout: default
last_updated: 2025-12-13
---

[← Back to Home](./index.md)

# Amateur Radio

This page outlines my amateur radio setup, how the radios tie into my home network and lab, and the scripts I use to support HF digital modes, APRS, and packet work. Each radio in the station fills a specific role across HF and VHF/UHF operation.

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
      src="./images/radio/ham-shack.png"
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

*Use the controls above to zoom and pan around the diagram. Scroll the mouse wheel over the diagram to zoom, and drag to pan.*

---

## Radio Equipment

### HF Radios

- **Icom IC-7300** – My primary HF radio for FT8/FT4, SSB, and general operation. This is the rig I use with WSJT-X in the shack.  
- **Xiegu G90** – A portable HF rig used for mobile and field operation. I occasionally run digital modes with it, but it’s mainly for portable work.

### VHF/UHF Radios

- **Kenwood TM-D700A** – Used for local repeaters, simplex, and general VHF/UHF activity.  
- **Yaesu FTM-3100R** – Dedicated APRS radio paired with Direwolf for packet decoding and iGate functions.

### Antennas and Feedlines
- HF wire antennas and tuners  
- Dual-band antennas for VHF/UHF and APRS  
- Proper grounding and feedline routing  

---

## Digital Modes and Data Work

### HF Digital Modes (WSJT-X)

WSJT-X runs on my lab systems and interfaces with the **IC-7300** for FT8/FT4 and other HF digital modes.

The **G90** is used for portable digital work when needed but is not part of the main digital setup.

### APRS and Packet (Direwolf)

Direwolf operates alongside the **FTM-3100R** for APRS and packet decoding.

This setup includes:
- USB soundcard interface  
- Virtual KISS interface for testing 
- APRS-IS forwarding  
- Packet filtering and parsing  
- APRX integration  

The **TM-D700A** is used for monitoring and voice, not APRS.

---

## Integration with the Home Network

Digital-mode applications run on Raspberry Pis or lab systems.

Key points:
- RF → radio → soundcard → Direwolf or WSJT-X
- Packet forwarding and monitoring inside the lab

---

## Scripts and Automation

I maintain several tools to support APRS, packet handling, and HF digital modes.

### APRS / Direwolf Utilities

| Script / Tool | Purpose | Repo |
|-------------------------|------------------------------------------------|------|
| Packet Injector | Sends KISS frames into Direwolf for testing. |      |
| APRS-IS Forwarder | Selective RF → APRS-IS forwarding. |      |

### Supporting Tools

| Script / Tool | Purpose | Repo |
|-------------------------------|---------------------------------------------------------|------|
| TCP Fan-Out Daemon | Distributes packet or decode data to multiple tools. |      |
| Audio Interface Helpers | Manages ALSA soundcard detection and stability. |      |  

---

## Future Expansion
- Additional HF automation  
- APRS telemetry  
- SDR receiver improvements  
- More packet-processing workflows  

---

## LoRa and ISM-Band Experiments

In addition to amateur radio, I also experiment with low-power LoRa nodes in the ISM bands. This isn’t part of my licensed HF or VHF/UHF activity, but it fits naturally alongside the rest of my RF and packet work.

My LoRa projects focus on:
- Building and testing low-power LoRa nodes  
- Evaluating link reliability around the property  
- Comparing different spreading factors and data rates  
- Measuring range, SNR, and general behavior in real conditions  

LoRa nodes report into my home lab, where I can monitor behavior, log received frames, and evaluate how well different configurations perform. Over time, I expect to expand this into more structured telemetry and data collection, but for now it remains an RF-focused experimentation platform rather than an application stack.

<div class="page-footer">

  [← Back to Home](./index.md)

  <span class="page-updated">
    Last updated: {{ page.last_updated }}
  </span>
</div>
