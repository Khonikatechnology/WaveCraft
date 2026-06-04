# WaveCraft

**AI-powered timing diagram generator for digital hardware design.**

🔗 **[Open WaveCraft → khonikatech.com/wavecraft](https://www.khonikatech.com/wavecraft)**

---

## What is WaveCraft?

WaveCraft turns plain-English descriptions into editable [WaveDrom](https://wavedrom.com) timing diagrams — instantly, in the browser, with no account required.

Describe your signals in plain English:

> *"clk1 is 100MHz, clk2 is 150MHz, data updates on the rising edge of clk2"*

Get a timing diagram:

![WaveCraft main interface](images/wavecraft-ui.png)

---

## How It Works

1. **Write Signal Names** — list your hardware signals (`clk valid ready data`)
2. **Describe timing in Chat** — plain English, no syntax required
3. **Get an instant diagram** — rendered WaveDrom SVG, editable JSON

![WaveCraft chat interface](images/wavecraft-chat.png)

---

## Features

- **Multi-clock domains** — specify frequencies, WaveCraft handles period ratios automatically
- **Timing annotations** — arrows between signals with latency labels
- **Context-aware editing** — add/remove/move signals without losing others
- **Protocol examples** — SPI, I2C, AXI, UART, APB, AXI-Stream, FIFO, BRAM, and more
- **Save as SVG or PNG**
- **Works on mobile and desktop**
- **Free, no sign-up required**

---

## Multi-Clock Domains

WaveCraft automatically handles frequency ratios between clocks — specify MHz values and it calculates the correct period relationships:

![Multi-clock diagram](images/wavecraft-clocks.png)

---

## Timing Annotations with Arrows

WaveCraft supports WaveDrom edge arrows to annotate latency, setup time, and timing relationships between signals:

![Arrow annotations](images/wavecraft-timing.png)

---

## Context-Aware Editing

Once a waveform is generated, you can iteratively refine it — move a signal by one cycle, add a new signal, or remove one — without losing the rest:

**Step 1 — Initial generation:**

![Context step 1](images/wavecraft-context1.png)

**Step 2 — Edit: move data_data forward by one cycle:**

![Context step 2](images/wavecraft-context2.png)

---

## Prompt Examples Page

Browse categorized examples for clock basics, handshakes, protocols, FPGA patterns, arrows, groups, and more:

![Prompt examples page](images/wavecraft-examples.png)

---

## Mobile

Works in Safari and Chrome on iOS and Android:

![Mobile view](images/wavecraft-phone.png)

---

## Try It

**[→ Open WaveCraft](https://www.khonikatech.com/wavecraft)**

**[→ Browse Prompt Examples](https://www.khonikatech.com/wavecraft/prompt-examples)**

---

*Built by [Khonika](https://www.khonikatech.com) · contact: info@khonika.com*
