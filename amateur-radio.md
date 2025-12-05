[← Back to Home](./index.md)

# Amateur Radio

This page outlines my amateur radio setup, how I have the equipment integrated into my home network and lab, and the scripts I use to support APRS, packet, and digital modes. The goal is to maintain a reliable RF setup while also experimenting with data and automation workflows.

---

# 1. Radio Equipment

## 1.1 Radios
I use a mix of VHF/UHF radios for local repeater work, simplex, and APRS/packet. I also run SDR receivers for monitoring and experimentation.  

## 1.2 Antennas and Feedlines
- Dual-band antennas mounted for consistent local coverage  
- Dedicated antennas for APRS and packet decoding  
- Coax, grounding, and mounting arranged for low noise and reliability  

---

# 2. Digital Modes and Data Work

## 2.1 APRS and Packet (Direwolf)
Direwolf acts as the primary TNC for APRS and packet operations. It handles both RF decoding and APRS-IS forwarding, and I also use a virtual KISS interface for injected packets and testing scripts.

Key components:
- Soundcard-based RF interface  
- Virtual KISS port (via `socat`)  
- Local scripts for parsing, filtering, and forwarding packets  
- APRX or other tools for handling iGate responsibilities when needed

## 2.2 WSJT-X (FT8/FT4)
My WSJT-X environment is configured for weak-signal digital modes. I run the newer 2.7.x builds, which include a JSON-based UDP protocol.  
I use custom scripts to parse these packets and track activity across different bands.

---

# 3. Integration with the Home Network

Most of the digital-mode tools run on Raspberry Pis or lab systems.  
These tie into my home network through the same segmentation model used across the rest of the environment.

Highlights:
- RF interfaces connected to Pis via USB soundcards  
- Direwolf and WSJT-X running on lab systems or Pis depending on the workload  
- Packet data forwarded internally for analysis  

---

# 4. Future Plans

Areas I want to continue exploring:
- Additional APRS telemetry  
- Expanded iGate support  
- HF data workflows  
- More SDR-based applications  

---

[← Back to Home](./index.md)
