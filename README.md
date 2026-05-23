VOLTMAP — EV Grid Intelligence Dashboard

An interactive real-time dashboard visualizing the US EV charging network, electricity grid demand, and ISO market pricing across the United States.
Live demo → voltmap-plum.vercel.app
<img width="1463" height="723" alt="Screenshot 2026-05-23 at 9 56 45 AM" src="https://github.com/user-attachments/assets/91891e45-e775-40d5-89a3-62a4947077e0" />
What it does
VOLTMAP is a grid intelligence tool that maps EV charging infrastructure against real energy market data — showing not just where chargers are, but how stressed the grid is at those locations and what electricity costs in each region right now.
It was built to answer a question grid operators and EV drivers both care about: when and where is it cheapest and safest to charge?

Features

Interactive real map — Leaflet.js with CartoDB dark tiles; pan and zoom anywhere in the world
30+ charging stations pinned at real US coordinates across all major metro areas
Live simulation — active sessions, grid draw (GW), and generation mix update in real time
ISO region pricing — locational marginal prices (LMP) for CAISO, ERCOT, PJM, MISO, NYISO, ISONE, and SPP, color-coded green → yellow → red by cost
Generation mix panel — tracks national energy sources (gas, wind, solar, nuclear, coal) with a draggable overlay you can move anywhere on the map
EV demand forecast — sparkline showing today's load curve with a live NOW marker, illustrating the duck curve effect
Grid stress indicators — utilization arc on each station marker; toggle the stress layer for heat radius overlays
Layer toggles — independently show/hide stations, demand zones, transmission corridors, and grid stress
Filters — filter stations by network (Tesla, Electrify America, ChargePoint) and power level (DC Fast 150kW+ vs Level 2 ≤22kW)
Station tooltips — hover any marker for port count, utilization, local LMP, and grid stress %
Data Story panel — contextual analysis of the duck curve, ERCOT isolation risk, and optimal charging windows


Tech stack

LayerTechnologyMapLeaflet.js 1.9.4Tile layerCartoDB Dark MatterFrontendVanilla HTML / CSS / JavaScriptFontsDM Sans + DM Mono (Google Fonts)DeploymentVercel
No frameworks, no build step, no dependencies to install — single index.html file.

Key concepts visualized

Locational Marginal Pricing (LMP) — electricity prices vary by region and time. CAISO and ISONE regularly hit $38+/MWh while ERCOT can drop to $16/MWh. The ISO panel tracks this in real time.
The duck curve — solar generation floods the grid mid-day then drops sharply at sunset, exactly when EV commuter demand spikes. The demand forecast sparkline shows this double-peak problem visually.
Grid stress — each station's utilization arc shows what percentage of ports are active. The stress layer overlays heat radii showing grid load pressure at each location.
Optimal charging window — 10AM–2PM, when solar is at peak output, prices are lowest, and grid stress is minimal.
