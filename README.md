# Satellite-and-Debris

A web‐based 3D visualization platform that displays real‐time orbital data for active satellites and space debris using CesiumJS and satellite.js. Satellites are rendered with smooth, interpolated paths, and debris fields can be toggled on/off by breakup group. TLE (Two‐Line Element) data is fetched from CelesTrak and cached (active satellites for 2 hours, debris for 6 hours) to minimize repeated network requests. A lightweight filter panel allows you to search by name and limit the number of satellites per orbit class (LEO, MEO, GEO). A “Real‐Time” button resets the view to the current UTC clock, while “Reset” clears all entities.

## Key Features

- **Live Satellite Orbits**  
  • Fetches “active” TLEs, groups by LEO/MEO/GEO, and displays up to N satellites per bucket.  
  • Smoothly interpolated paths (Hermite) over the next 30 seconds, updating each clock tick.  

- **Debris Toggles**  
  • Four breakup catalogs (Cosmos-2251, Cosmos-1408, Fengyun-1C, Iridium-33).  
  • Master “Show Debris” checkbox plus individual group toggles.  
  • Each group fetched only once every 6 hours to save bandwidth.  

- **Search & Filter Panel**  
  • Search by name (substring match) and see up to 50 results.  
  • Filter by orbit type (LEO/MEO/GEO) and cap how many per orbit.  
  • “Apply” clears and reloads the viewer with your criteria.  

- **Clock Controls**  
  • **Real-Time (Today)** button jumps to current UTC and runs the clock at 1× speed.  
  • **Reset** button clears all satellites and debris from the globe.  
