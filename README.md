# urban-parking-dynamic-pricing

# Summer Analytics 2025

A real-time dynamic pricing engine built for urban parking lots using **Numpy**, **Pandas**, and **Pathway**, aimed at optimizing space utilization by adjusting prices based on demand, traffic, and queue metrics.

---

##  Overview

In modern cities, parking demand varies by time, traffic, and surrounding activity. Static pricing leads to inefficiencies like overcrowding or underuse. This project simulates **dynamic pricing strategies** for 14 parking spaces over 73 days and 18 time slots/day using machine learning-inspired logic built from scratch.

Key objectives:
- Dynamically price each parking space starting from a $10 base
- Ensure smooth, explainable variation using real-time signals
- Optionally reroute vehicles when nearby lots are cheaper or free

---

##  Tech Stack

| Tool / Library    | Purpose                            |
|-------------------|------------------------------------|
| Python (Colab)    | Development environment            |
| Pandas & Numpy    | Data handling & calculations       |
| Pathway           | Real-time streaming simulation     |
| Matplotlib        | Static data visualization          |
| Bokeh             | Interactive real-time visualization|
| Mermaid.js        | Architecture diagram               |
| GitHub            | Version control and sharing        |

---

##  Architecture Diagram (Mermaid)

```mermaid
flowchart TD
    subgraph Real-Time Stream
        A[Raw Dataset (CSV)] --> B[Pathway Streaming Engine]
    end

    subgraph Processing Logic
        B --> C[Data Preprocessing (Timestamp Sort)]
        C --> D[Model 1: Linear Pricing]
        C --> E[Model 2: Demand-Based Pricing]
        C --> F[Model 3: Competitive Pricing]
    end

    subgraph Output
        D & E & F --> G[Pricing Output Table]
        G --> H[Bokeh Visual Dashboard]
        G --> I[Optional Rerouting Suggestions]
    end
