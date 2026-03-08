# SkyIQ

**A fuel planning and optimization platform for Part 135 aviation operators — reducing fuel costs through data-driven route optimization, real-time pricing intelligence, and predictive analytics.**

🔗 [skyiq.net](https://www.skyiq.net) · [Live App](https://app.skyiq.net) · Trademark Pending · Patent Pending (USPTO Non-Provisional Utility Patent Filed)

---

## The Problem

Part 135 charter and cargo operators make fuel purchasing decisions based on habit and guesswork. Pilots fuel up at whatever FBO is convenient. Dispatchers don't have time to compare prices across airports. Nobody is optimizing fuel stops against route efficiency, aircraft performance, and real-time pricing — even though fuel is typically the single largest variable operating cost.

The result: operators overpay on fuel by thousands of dollars per trip, every trip, across their entire fleet.

---

## The Solution

SkyIQ is a fuel planning optimization platform that combines real-time fuel pricing data, aircraft performance specs, route analysis, and predictive modeling to recommend the most cost-efficient fueling strategy for every flight.

**For Dispatchers & Flight Planners:** Input a route and aircraft type. SkyIQ analyzes every possible fuel stop along the route, cross-references real-time fuel prices, factors in aircraft range and payload constraints, and recommends the optimal fueling plan — showing exactly how much money each option saves.

**For Fleet Managers:** Dashboard-level visibility into fleet-wide fuel spend, savings opportunities, and historical optimization data across all aircraft and routes.

**For Operators:** Automated fuel cost intelligence that integrates into existing dispatch workflows without requiring pilots or dispatchers to change how they work.

---

## My Role

**Co-Founder — Product, Architecture & Design.** I own the product vision, system architecture, brand, UX, and go-to-market. My co-founder built the core fuel planning logic and optimization algorithms. We partnered with the same development team we used for Raising Reimagined to bring the full platform to production.

What that looked like in practice:

- Identified the problem through direct experience in Part 135 aviation operations
- Defined the product requirements and system architecture: modular system separating data ingestion, AI parsing, optimization, and user-facing components with documented interaction flows
- Supported development of the core fuel optimization logic alongside my co-founder, who wrote the planning algorithms
- Created all wireframes and UX designs for the application
- Designed the entire brand identity — logo, color system, typography, business cards, marketing mailers
- Built the investor/customer pitch materials — one-pager, customer deck, full investor deck
- Managed the development partnership to bring the product from prototype to live application
- Filed for trademark protection and non-provisional utility patent (19 claims, filed with USPTO August 2025)

---

## Product Architecture

SkyIQ is built as a modular system. I designed the architecture to separate concerns across independent components — data ingestion, user interface, optimization, and output — so that each piece can evolve without requiring a full rewrite.

The core workflow: a dispatcher uploads a PDF itinerary or enters trip details manually. AI parses and extracts all pertinent trip data automatically. The system then pulls in real-time fuel pricing and aircraft performance data, runs the optimization through a modified Dijkstra's algorithm, and outputs a cost-ranked fueling plan. The dispatcher can review, override, and finalize before exporting.

Key architectural decisions I made early on: keeping modules loosely coupled so data sources could be swapped without rearchitecting, designing for mobile-first since pilots and dispatchers work from the ramp, and building in user override points because experienced operators need to trust (and verify) the recommendations.

### Module Interaction Diagram

<p align="center">
  <img src="artifacts/module-interaction.png" alt="SkyIQ Module Interaction Diagram" width="700"/>
</p>

### Module-Level Processes

<p align="center">
  <img src="artifacts/module-processes.png" alt="SkyIQ Module-Level Processes" width="700"/>
</p>

<details>
<summary>📐 Diagram Legend</summary>
<br/>
<p align="center">
  <img src="artifacts/legend.png" alt="Diagram Legend" width="500"/>
</p>
</details>

---

## How It Works

The platform combines two core technical capabilities:

**AI-Powered Itinerary Parsing:** Dispatchers can upload a PDF itinerary or enter trip details manually. The system uses AI to parse and extract all pertinent trip information — airports, legs, passengers, weights, fuel prices — and auto-fills the planning interface. This eliminates the manual data entry that slows down traditional dispatch workflows.

**Optimization Engine (Modified Dijkstra's Algorithm):** My co-founder developed the core fuel planning logic in Python. The algorithm uses a modified version of Dijkstra's shortest-path algorithm to find the lowest-cost fueling strategy across all viable stop combinations. It factors in real-time fuel pricing across FBOs, aircraft-specific fuel burn rates, range and payload constraints, and fee structures — then ranks options by total cost and presents the optimal strategy with a savings comparison.

This prototype logic proved the concept before we partnered with our development team to build the full platform.

### User Journey Flow

<p align="center">
  <img src="artifacts/user-journey.png" alt="SkyIQ User Journey Flow" width="700"/>
</p>

---

## Brand & Design

I designed everything visual about SkyIQ — logo, color palette, typography, wireframes, marketing materials, and pitch collateral. This wasn't outsourced. I believe founders should deeply understand their product's visual language, and I wanted every touchpoint to communicate precision and trust (critical in aviation).

### Brand Identity

<p align="center">
  <img src="artifacts/brand-identity.png" alt="SkyIQ Brand Identity" width="700"/>
</p>

### Wireframes

<p align="center">
  <img src="artifacts/wireframe.png" alt="SkyIQ Application Wireframes" width="700"/>
</p>

### One-Pager

<p align="center">
  <img src="artifacts/one-pager.png" alt="SkyIQ One-Pager" width="700"/>
</p>

---

## Product Thinking

**Domain Expertise → Product Insight:** My background in aviation operations (Part 135 dispatch, cargo planning through OnFly Air) meant I didn't need to guess at the problem. I lived it. Every product decision was informed by real dispatch workflows and real operator pain points.

**Prove the Logic First:** Before any UI or platform work, my co-founder built the optimization algorithm in Python to prove the math worked. I defined the product requirements and constraints the algorithm needed to satisfy. This prototype validated that meaningful savings existed before we invested in building a full application.

**Modular Architecture:** Designed the system as independent modules from day one. Fuel pricing data sources change. Aircraft specs get updated. Weather APIs evolve. By keeping each component independent, the platform can adapt without a rewrite.

**Trust Through Precision:** In aviation, software needs to be trustworthy. The UX prioritizes showing the work — dispatchers can see exactly why SkyIQ recommends a specific fuel stop, what the alternatives cost, and what assumptions the model is making. No black boxes.

---

## Tech Stack

- Python (core optimization logic — modified Dijkstra's algorithm)
- AI-powered PDF parsing and itinerary extraction
- Web-based SaaS application
- Real-time fuel pricing data integration
- Aircraft performance database
- Route analysis and mapping
- Modular architecture with independent data services

---

## Status

- **Live application** at [app.skyiq.net](https://app.skyiq.net)
- **Patent pending** — Non-provisional utility patent filed with USPTO (19 claims)
- **Trademark pending** for SkyIQ brand
- Active development with roadmap for fleet-level analytics and API integrations

---

*Built by [Paige Miller](https://github.com/paige-millz) — Co-Founder, Product & Design*
